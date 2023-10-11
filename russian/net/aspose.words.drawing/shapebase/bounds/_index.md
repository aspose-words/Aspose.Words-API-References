---
title: ShapeBase.Bounds
second_title: Справочник по API Aspose.Words для .NET
description: ShapeBase свойство. Получает или задает расположение и размер содержащего блока фигуры.
type: docs
weight: 70
url: /ru/net/aspose.words.drawing/shapebase/bounds/
---
## ShapeBase.Bounds property

Получает или задает расположение и размер содержащего блока фигуры.

```csharp
public RectangleF Bounds { get; set; }
```

### Примечания

Игнорирует блокировку соотношения сторон при настройке.

Для фигуры верхнего уровня значение указывается в пунктах и относительно привязки формы.

Для фигур в группе значение находится в координатном пространстве и единицах родительской группы.

### Примеры

Показывает, как проверить форму, содержащую границы блоков.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.Line, RelativeHorizontalPosition.LeftMargin, 50,
    RelativeVerticalPosition.TopMargin, 50, 100, 100, WrapType.None);
shape.StrokeColor = Color.Orange;

// Несмотря на то, что сама строка занимает мало места на странице документа,
// он занимает прямоугольный содержащий блок, размер которого мы можем определить с помощью свойства «Границы».
Assert.AreEqual(new RectangleF(50, 50, 100, 100), shape.Bounds);
Assert.AreEqual(new RectangleF(50, 50, 100, 100), shape.BoundsInPoints);

// Создайте фигуру группы, а затем установите размер содержащего ее блока с помощью свойства «Bounds».
GroupShape group = new GroupShape(doc);
group.Bounds = new RectangleF(0, 100, 250, 250);

Assert.AreEqual(new RectangleF(0, 100, 250, 250), group.BoundsInPoints);

// Создаем прямоугольник, проверяем размер его ограничивающего блока, а затем добавляем его в фигуру группы.
shape = new Shape(doc, ShapeType.Rectangle)
{
    Width = 100,
    Height = 100,
    Left = 700,
    Top = 700
};

Assert.AreEqual(new RectangleF(700, 700, 100, 100), shape.BoundsInPoints);

group.AppendChild(shape);

// Координатная плоскость фигуры группы имеет начало в верхнем левом углу содержащего ее блока,
// и координаты x и y (1000, 1000) в правом нижнем углу.
// Размер нашей фигуры группы 250x250 точек, поэтому каждые 4 точки на координатной плоскости фигуры группы
// преобразуется в 1pt в координатной плоскости тела документа.
// Каждая фигура, которую мы вставляем, также уменьшится в размере в 4 раза.
// Изменение свойства BoundsInPoints фигуры отразит это.
Assert.AreEqual(new RectangleF(175, 275, 25, 25), shape.BoundsInPoints);

doc.FirstSection.Body.FirstParagraph.AppendChild(group);

// Вставляем фигуру и размещаем ее за пределами блока, содержащего фигуру группы.
shape = new Shape(doc, ShapeType.Rectangle)
{
    Width = 100,
    Height = 100,
    Left = 1000,
    Top = 1000
};

group.AppendChild(shape);

// Площадь фигуры группы в теле документа увеличилась, но содержащий ее блок остался прежним.
Assert.AreEqual(new RectangleF(0, 100, 250, 250), group.BoundsInPoints);
Assert.AreEqual(new RectangleF(250, 350, 25, 25), shape.BoundsInPoints);

doc.Save(ArtifactsDir + "Shape.Bounds.docx");
```

Показывает, как создать и заполнить фигуру группы.

```csharp
Document doc = new Document();

// Создаем фигуру группы. Фигура группы может отображать коллекцию узлов дочерней фигуры.
// В Microsoft Word щелчок внутри границы фигуры группы или на одной из дочерних фигур группы приведет к
// выбираем все остальные дочерние фигуры в этой группе и позволяем нам масштабировать и перемещать все фигуры одновременно.
GroupShape group = new GroupShape(doc);

Assert.AreEqual(WrapType.None, group.WrapType);

// Создайте групповую фигуру размером 400 x 400 точек и поместите ее в начало координат плавающей фигуры документа.
group.Bounds = new RectangleF(0, 0, 400, 400);

// Установите размер внутренней координатной плоскости группы 500 x 500pt. 
// Верхний левый угол группы будет иметь координаты x и y (0, 0),
// и нижний правый угол будет иметь координаты x и y (500, 500).
group.CoordSize = new Size(500, 500);

// Устанавливаем координаты верхнего левого угла группы (-250, -250). 
// Центр группы теперь будет иметь координаты x и y (0, 0),
// и нижний правый угол будет в (250, 250).
group.CoordOrigin = new Point(-250, -250);

// Создайте прямоугольник, который будет отображать границу этой формы группы, и добавьте его в группу.
group.AppendChild(new Shape(doc, ShapeType.Rectangle)
{
    Width = group.CoordSize.Width,
    Height = group.CoordSize.Height,
    Left = group.CoordOrigin.X,
    Top = group.CoordOrigin.Y
});

// Как только фигура становится частью фигуры группы, мы можем получить к ней доступ как к дочернему узлу, а затем изменить ее.
((Shape)group.GetChild(NodeType.Shape, 0, true)).Stroke.DashStyle = DashStyle.Dash;

// Создаем маленькую красную звезду и вставляем ее в группу.
// Выравниваем фигуру по началу координат группы, которую мы переместили в центр.
group.AppendChild(new Shape(doc, ShapeType.Star)
{
    Width = 20,
    Height = 20,
    Left = -10,
    Top = -10,
    FillColor = Color.Red
});

// Вставляем прямоугольник, а затем вставляем прямоугольник чуть меньшего размера в то же место, где находится изображение. 
// Новые фигуры, которые мы добавляем в группу, перекрывают старые фигуры. Голубой прямоугольник частично перекроет красную звезду.
// и тогда фигура с изображением перекроет голубой прямоугольник, используя его в качестве рамки.
// Мы не можем использовать свойства фигур «ZOrder» для управления их расположением внутри групповой фигуры. 
group.AppendChild(new Shape(doc, ShapeType.Rectangle)
{
    Width = 250,
    Height = 250,
    Left = -250,
    Top = -250,
    FillColor = Color.LightBlue
});

group.AppendChild(new Shape(doc, ShapeType.Image)
{
    Width = 200,
    Height = 200,
    Left = -225,
    Top = -225
});

((Shape)group.GetChild(NodeType.Shape, 3, true)).ImageData.SetImage(ImageDir + "Logo.jpg");

// Вставляем текстовое поле в фигуру группы. Установите свойство «Left», чтобы правый край текстового поля
// касается правой границы формы группы. Установите свойство Top, чтобы текстовое поле располагалось снаружи.
// граница фигуры группы, верхний размер которой выровнен вдоль нижнего поля фигуры группы.
group.AppendChild(new Shape(doc, ShapeType.TextBox)
{
    Width = 200,
    Height = 50,
    Left = group.CoordSize.Width + group.CoordOrigin.X - 200,
    Top = group.CoordSize.Height + group.CoordOrigin.Y
});

DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertNode(group);
builder.MoveTo(((Shape)group.GetChild(NodeType.Shape, 4, true)).AppendChild(new Paragraph(doc)));
builder.Write("Hello world!");

doc.Save(ArtifactsDir + "Shape.GroupShape.docx");
```

### Смотрите также

* class [ShapeBase](../)
* пространство имен [Aspose.Words.Drawing](../../shapebase/)
* сборка [Aspose.Words](../../../)


