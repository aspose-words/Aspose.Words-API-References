---
title: ShapeBase.CoordSize
second_title: Справочник по API Aspose.Words для .NET
description: ShapeBase свойство. Ширина и высота координатного пространства внутри содержащего блока этой формы.
type: docs
weight: 120
url: /ru/net/aspose.words.drawing/shapebase/coordsize/
---
## ShapeBase.CoordSize property

Ширина и высота координатного пространства внутри содержащего блока этой формы.

```csharp
public Size CoordSize { get; set; }
```

### Примечания

Значение по умолчанию — (1000, 1000).

### Примеры

Показывает, как преобразовать местоположение координат X и Y на координатной плоскости фигуры в местоположение на координатной плоскости родительской фигуры.

```csharp
Document doc = new Document();

// Вставляем фигуру группы и размещаем ее на 100 пунктов ниже и правее
// исходная точка координат x и Y документа.
GroupShape group = new GroupShape(doc);
group.Bounds = new RectangleF(100, 100, 500, 500);

// Используйте метод «LocalToParent», чтобы определить, что (0, 0) во внутренних координатах x и y группы
// лежит в (100, 100) системы координат родительской фигуры. Родителем формы группы является сам документ.
Assert.AreEqual(new PointF(100, 100), group.LocalToParent(new PointF(0, 0)));

// По умолчанию внутренняя координатная плоскость фигуры имеет верхний левый угол (0, 0),
// и нижний правый угол (1000, 1000). Из-за своего размера наша групповая фигура занимает площадь 500 x 500 пикселей.
// в плоскости документа. Это означает, что перемещение на 1 пт в координатной плоскости документа будет смещаться.
// к перемещению на 2 пункта по координатной плоскости группы.
Assert.AreEqual(new PointF(150, 150), group.LocalToParent(new PointF(100, 100)));
Assert.AreEqual(new PointF(200, 200), group.LocalToParent(new PointF(200, 200)));
Assert.AreEqual(new PointF(250, 250), group.LocalToParent(new PointF(300, 300)));

// Перемещаем начало осей x и y фигуры группы из верхнего левого угла в центр.
// Это еще больше сместит внутренние координаты группы относительно координат документа.
group.CoordOrigin = new Point(-250, -250);

Assert.AreEqual(new PointF(375, 375), group.LocalToParent(new PointF(300, 300)));

// Изменение масштаба координатной плоскости также повлияет на относительные местоположения.
group.CoordSize = new Size(500, 500);

Assert.AreEqual(new PointF(650, 650), group.LocalToParent(new PointF(300, 300)));

// Если мы хотим добавить фигуру в эту группу, определяя ее местоположение на основе местоположения в документе,
// нам нужно сначала подтвердить местоположение в форме группы, которое будет соответствовать местоположению документа.
Assert.AreEqual(new PointF(700, 700), group.LocalToParent(new PointF(350, 350)));

Shape shape = new Shape(doc, ShapeType.Rectangle)
{
    Width = 100,
    Height = 100,
    Left = 700,
    Top = 700
};

group.AppendChild(shape);
doc.FirstSection.Body.FirstParagraph.AppendChild(group);

doc.Save(ArtifactsDir + "Shape.LocalToParent.docx");
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


