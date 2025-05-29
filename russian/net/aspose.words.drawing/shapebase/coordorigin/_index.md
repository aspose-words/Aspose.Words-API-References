---
title: ShapeBase.CoordOrigin
linktitle: CoordOrigin
articleTitle: CoordOrigin
second_title: Aspose.Words для .NET
description: Откройте для себя свойство ShapeBase CoordOrigin для оптимизации ваших проектов. Получите доступ к точным координатам верхнего левого угла содержащего блока вашей фигуры.
type: docs
weight: 110
url: /ru/net/aspose.words.drawing/shapebase/coordorigin/
---
## ShapeBase.CoordOrigin property

Координаты в верхнем левом углу содержащего блока этой формы.

```csharp
public Point CoordOrigin { get; set; }
```

## Примечания

Значение по умолчанию — (0,0).

## Примеры

Показывает, как перевести координаты x и y на координатной плоскости фигуры в координатную плоскость родительской фигуры.

```csharp
Document doc = new Document();

// Вставьте групповую фигуру и разместите ее на 100 пунктов ниже и правее
// исходная точка координат x и Y документа.
GroupShape group = new GroupShape(doc);
group.Bounds = new RectangleF(100, 100, 500, 500);

// Используйте метод "LocalToParent", чтобы определить (0, 0) во внутренних координатах x и y группы
// лежит на (100, 100) системы координат родительской фигуры. Родителем групповой фигуры является сам документ.
Assert.AreEqual(new PointF(100, 100), group.LocalToParent(new PointF(0, 0)));

// По умолчанию внутренняя координатная плоскость фигуры имеет верхний левый угол в точке (0, 0),
// и нижний правый угол в (1000, 1000). Из-за своего размера наша групповая фигура занимает область 500pt x 500pt
// в плоскости документа. Это означает, что перемещение на 1pt в координатной плоскости документа переместит
// к перемещению на 2 точки на координатной плоскости групповой фигуры.
Assert.AreEqual(new PointF(150, 150), group.LocalToParent(new PointF(100, 100)));
Assert.AreEqual(new PointF(200, 200), group.LocalToParent(new PointF(200, 200)));
Assert.AreEqual(new PointF(250, 250), group.LocalToParent(new PointF(300, 300)));

// Перемещаем начало осей x и y групповой фигуры из верхнего левого угла в центр.
// Это еще больше сместит внутренние координаты группы относительно координат документа.
group.CoordOrigin = new Point(-250, -250);

Assert.AreEqual(new PointF(375, 375), group.LocalToParent(new PointF(300, 300)));

// Изменение масштаба координатной плоскости также повлияет на относительное местоположение.
group.CoordSize = new Size(500, 500);

Assert.AreEqual(new PointF(650, 650), group.LocalToParent(new PointF(300, 300)));

// Если мы хотим добавить фигуру в эту группу, определив ее местоположение на основе местоположения в документе,
// нам сначала нужно будет подтвердить местоположение в форме группы, которое будет соответствовать местоположению документа.
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
