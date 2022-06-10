---
title: CoordOrigin
second_title: Справочник по API Aspose.Words для .NET
description: Координаты в верхнем левом углу содержащего блока этой формы.
type: docs
weight: 110
url: /ru/net/aspose.words.drawing/shapebase/coordorigin/
---
## ShapeBase.CoordOrigin property

Координаты в верхнем левом углу содержащего блока этой формы.

```csharp
public Point CoordOrigin { get; set; }
```

### Примечания

Значение по умолчанию (0,0).

### Примеры

Показывает, как перевести координаты x и y на координатной плоскости фигуры в положение на координатной плоскости родительской фигуры.

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

* class [ShapeBase](../../shapebase)
* namespace [Aspose.Words.Drawing](../../shapebase)
* assembly [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
