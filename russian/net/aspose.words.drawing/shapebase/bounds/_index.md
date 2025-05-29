---
title: ShapeBase.Bounds
linktitle: Bounds
articleTitle: Bounds
second_title: Aspose.Words для .NET
description: Откройте для себя свойство ShapeBase Bounds, которое позволит вам легко управлять местоположением и размером вашей фигуры, повышая точность и эффективность вашего дизайна.
type: docs
weight: 70
url: /ru/net/aspose.words.drawing/shapebase/bounds/
---
## ShapeBase.Bounds property

Возвращает или задает местоположение и размер содержащего блока фигуры.

```csharp
public RectangleF Bounds { get; set; }
```

## Примечания

Игнорирует блокировку соотношения сторон при настройке.

Для фигуры верхнего уровня значение указывается в пунктах и относительно привязки фигуры.

Для фигур в группе значение находится в координатном пространстве и единицах измерения родительской группы.

## Примеры

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

// Создаем групповую фигуру, а затем задаем размер ее содержащего блока с помощью свойства «Границы».
GroupShape group = new GroupShape(doc);
group.Bounds = new RectangleF(0, 100, 250, 250);

Assert.AreEqual(new RectangleF(0, 100, 250, 250), group.BoundsInPoints);

// Создаем прямоугольник, проверяем размер его ограничивающего блока, а затем добавляем его в групповую фигуру.
shape = new Shape(doc, ShapeType.Rectangle)
{
    Width = 100,
    Height = 100,
    Left = 700,
    Top = 700
};

Assert.AreEqual(new RectangleF(700, 700, 100, 100), shape.BoundsInPoints);

group.AppendChild(shape);

// Координатная плоскость групповой фигуры имеет начало в верхнем левом углу содержащего ее блока,
// и координаты x и y (1000, 1000) в нижнем правом углу.
// Размер нашей групповой фигуры составляет 250x250 точек, поэтому каждые 4 точки на координатной плоскости групповой фигуры
// преобразуется в 1pt в координатной плоскости тела документа.
// Каждая вставленная нами фигура также уменьшится в размере в 4 раза.
// Изменение свойства фигуры "BoundsInPoints" отразит это.
Assert.AreEqual(new RectangleF(175, 275, 25, 25), shape.BoundsInPoints);

doc.FirstSection.Body.FirstParagraph.AppendChild(group);

// Вставьте фигуру и поместите ее за пределами границ содержащего ее блока.
shape = new Shape(doc, ShapeType.Rectangle)
{
    Width = 100,
    Height = 100,
    Left = 1000,
    Top = 1000
};

group.AppendChild(shape);

// Размер групповой фигуры в теле документа увеличился, но содержащий ее блок остался прежним.
Assert.AreEqual(new RectangleF(0, 100, 250, 250), group.BoundsInPoints);
Assert.AreEqual(new RectangleF(250, 350, 25, 25), shape.BoundsInPoints);

doc.Save(ArtifactsDir + "Shape.Bounds.docx");
```

Показывает, как создать и заполнить групповую фигуру.

```csharp
Document doc = new Document();

// Создать групповую фигуру. Групповая фигура может отображать коллекцию дочерних узлов фигуры.
// В Microsoft Word щелчок внутри границы групповой фигуры или на одной из дочерних фигур групповой фигуры приведет к
// выбираем все остальные дочерние фигуры в этой группе и позволяем масштабировать и перемещать все фигуры одновременно.
GroupShape group = new GroupShape(doc);

Assert.AreEqual(WrapType.None, group.WrapType);

// Создаем групповую фигуру размером 400 x 400 точек и помещаем ее в начало координат плавающей фигуры документа.
group.Bounds = new RectangleF(0, 0, 400, 400);

 // Устанавливаем размер внутренней координатной плоскости группы 500 x 500 точек.
// Верхний левый угол группы будет иметь координаты x и y (0, 0),
// а нижний правый угол будет иметь координаты x и y (500, 500).
group.CoordSize = new Size(500, 500);

 // Установите координаты верхнего левого угла группы на (-250, -250).
// Центр группы теперь будет иметь координаты x и y, равные (0, 0),
// а нижний правый угол будет в точке (250, 250).
group.CoordOrigin = new Point(-250, -250);

// Создаем прямоугольник, который будет отображать границу этой групповой фигуры, и добавляем его в группу.
Shape child1 = new Shape(doc, ShapeType.Rectangle)
{
    Width = group.CoordSize.Width,
    Height = group.CoordSize.Height,
    Left = group.CoordOrigin.X,
    Top = group.CoordOrigin.Y
};
group.AppendChild(child1);

// Как только фигура становится частью групповой фигуры, мы можем получить к ней доступ как к дочернему узлу, а затем изменить ее.
((Shape)group.GetChild(NodeType.Shape, 0, true)).Stroke.DashStyle = DashStyle.Dash;

// Создаем маленькую красную звездочку и вставляем ее в группу.
// Выровняйте фигуру с началом координат группы, которое мы переместили в центр.
Shape child2 = new Shape(doc, ShapeType.Star)
{
    Width = 20,
    Height = 20,
    Left = -10,
    Top = -10,
    FillColor = Color.Red
};
group.AppendChild(child2);

// Вставьте прямоугольник, а затем вставьте немного меньший прямоугольник в то же место с изображением.
// Новые формы, которые мы добавляем в группу, перекрывают старые формы. Светло-голубой прямоугольник частично перекроет красную звезду,
// и затем фигура с изображением наложится на светло-голубой прямоугольник, используя его как рамку.
// Мы не можем использовать свойства фигур «ZOrder» для управления их расположением в групповой фигуре.
Shape child3 = new Shape(doc, ShapeType.Rectangle)
{
    Width = 250,
    Height = 250,
    Left = -250,
    Top = -250,
    FillColor = Color.LightBlue
};
group.AppendChild(child3);

Shape child4 = new Shape(doc, ShapeType.Image)
{
    Width = 200,
    Height = 200,
    Left = -225,
    Top = -225
};
group.AppendChild(child4);

((Shape)group.GetChild(NodeType.Shape, 3, true)).ImageData.SetImage(ImageDir + "Logo.jpg");

// Вставьте текстовое поле в групповую фигуру. Установите свойство "Left" так, чтобы правый край текстового поля
// касается правой границы формы группы. Установите свойство "Top" так, чтобы текстовое поле располагалось снаружи
// граница групповой фигуры, верхний размер которой выровнен по нижнему краю групповой фигуры.
Shape child5 = new Shape(doc, ShapeType.TextBox)
{
    Width = 200,
    Height = 50,
    Left = group.CoordSize.Width + group.CoordOrigin.X - 200,
    Top = group.CoordSize.Height + group.CoordOrigin.Y
};
group.AppendChild(child5);

DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertNode(group);
builder.MoveTo(((Shape)group.GetChild(NodeType.Shape, 4, true)).AppendChild(new Paragraph(doc)));
builder.Write("Hello world!");

doc.Save(ArtifactsDir + "Shape.GroupShape.docx");
```

### Смотрите также

* class [ShapeBase](../)
* пространство имен [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* сборка [Aspose.Words](../../../)
