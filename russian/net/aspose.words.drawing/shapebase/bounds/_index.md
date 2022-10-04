---
title: Bounds
second_title: Справочник по API Aspose.Words для .NET
description: Получает или задает расположение и размер содержащего блока фигуры.
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

Для формы верхнего уровня значение указывается в пунктах и относительно привязки формы.

Для фигур в группе значение находится в пространстве координат и единицах родительской группы.

### Примеры

Показывает, как проверить форму, содержащую границы блоков.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.Line, RelativeHorizontalPosition.LeftMargin, 50,
    RelativeVerticalPosition.TopMargin, 50, 100, 100, WrapType.None);
shape.StrokeColor = Color.Orange;

// Несмотря на то, что сама строка занимает мало места на странице документа,
// он занимает прямоугольный содержащий блок, размер которого мы можем определить с помощью свойств "Границы".
Assert.AreEqual(new RectangleF(50, 50, 100, 100), shape.Bounds);
Assert.AreEqual(new RectangleF(50, 50, 100, 100), shape.BoundsInPoints);

// Создайте фигуру группы, а затем установите размер содержащего ее блока с помощью свойства «Границы».
GroupShape group = new GroupShape(doc);
group.Bounds = new RectangleF(0, 100, 250, 250);

Assert.AreEqual(new RectangleF(0, 100, 250, 250), group.BoundsInPoints);

// Создайте прямоугольник, проверьте размер его ограничивающего блока, а затем добавьте его к фигуре группы.
shape = new Shape(doc, ShapeType.Rectangle)
{
    Width = 100,
    Height = 100,
    Left = 700,
    Top = 700
};

Assert.AreEqual(new RectangleF(700, 700, 100, 100), shape.BoundsInPoints);

group.AppendChild(shape);

// Координатная плоскость групповой формы имеет начало в верхнем левом углу содержащего ее блока,
// и координаты x и y (1000, 1000) в правом нижнем углу.
// Наша фигура группы имеет размер 250x250 точек, поэтому каждые 4 точки на координатной плоскости формы группы
// преобразуется в 1 точку в координатной плоскости тела документа.
// Каждая фигура, которую мы вставляем, также уменьшается в размере в 4 раза.
// Это отразится на изменении свойства "BoundsInPoints" фигуры.
Assert.AreEqual(new RectangleF(175, 275, 25, 25), shape.BoundsInPoints);

doc.FirstSection.Body.FirstParagraph.AppendChild(group);

// Вставьте фигуру и поместите ее за пределы блока, содержащего фигуру группы.
shape = new Shape(doc, ShapeType.Rectangle)
{
    Width = 100,
    Height = 100,
    Left = 1000,
    Top = 1000
};

group.AppendChild(shape);

// Размер фигуры группы в теле документа увеличился, но содержащий ее блок остался прежним.
Assert.AreEqual(new RectangleF(0, 100, 250, 250), group.BoundsInPoints);
Assert.AreEqual(new RectangleF(250, 350, 25, 25), shape.BoundsInPoints);

doc.Save(ArtifactsDir + "Shape.Bounds.docx");
```

Показывает, как создать и заполнить фигуру группы.

```csharp
Document doc = new Document();

// Создаем фигуру группы. Фигура группы может отображать коллекцию узлов дочерней фигуры.
// В Microsoft Word щелчок в пределах границы фигуры группы или на одной из дочерних фигур фигуры группы приведет к
// выбираем все остальные дочерние фигуры в этой группе и позволяем масштабировать и перемещать все фигуры одновременно.
GroupShape group = new GroupShape(doc);

Assert.AreEqual(WrapType.None, group.WrapType);

// Создайте фигуру группы 400 x 400 пикселей и поместите ее в начало координат плавающей формы документа.
group.Bounds = new RectangleF(0, 0, 400, 400);

 // Установите размер внутренней координатной плоскости группы на 500 x 500pt.
// Верхний левый угол группы будет иметь координаты x и y (0, 0),
// и нижний правый угол будет иметь координаты x и y (500, 500).
group.CoordSize = new Size(500, 500);

 // Установите координаты верхнего левого угла группы на (-250, -250).
// Центр группы теперь будет иметь значение координат x и y (0, 0),
// и нижний правый угол будет на (250, 250).
group.CoordOrigin = new Point(-250, -250);

// Создадим прямоугольник, который будет отображать границу этой групповой фигуры, и добавим его в группу.
group.AppendChild(new Shape(doc, ShapeType.Rectangle)
{
    Width = group.CoordSize.Width,
    Height = group.CoordSize.Height,
    Left = group.CoordOrigin.X,
    Top = group.CoordOrigin.Y
});

// Когда фигура становится частью групповой фигуры, мы можем получить к ней доступ как к дочернему узлу, а затем изменить ее.
((Shape)group.GetChild(NodeType.Shape, 0, true)).Stroke.DashStyle = DashStyle.Dash;

// Создаем маленькую красную звезду и вставляем ее в группу.
// Выровняйте фигуру с началом координат группы, которое мы переместили в центр.
group.AppendChild(new Shape(doc, ShapeType.Star)
{
    Width = 20,
    Height = 20,
    Left = -10,
    Top = -10,
    FillColor = Color.Red
});

 // Вставьте прямоугольник, а затем вставьте прямоугольник чуть меньшего размера в то же место, что и изображение.
// Новые фигуры, которые мы добавляем в группу, перекрывают старые фигуры. Светло-голубой прямоугольник частично перекроет красную звезду,
// и тогда фигура с изображением наложится на голубой прямоугольник, используя его как рамку.
 // Мы не можем использовать свойства "ZOrder" фигур для управления их расположением внутри групповой фигуры.
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

// Вставляем текстовое поле в фигуру группы. Установите свойство «Левый», чтобы правый край текстового поля
// касается правой границы формы группы. Установите свойство «Сверху», чтобы текстовое поле находилось снаружи
// граница фигуры группы, верхний размер которой выровнен по нижнему полю формы группы.
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

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
