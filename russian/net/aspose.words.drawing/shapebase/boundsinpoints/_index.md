---
title: ShapeBase.BoundsInPoints
linktitle: BoundsInPoints
articleTitle: BoundsInPoints
second_title: Aspose.Words для .NET
description: ShapeBase BoundsInPoints свойство. Получает местоположение и размер содержащего блока фигуры в точках относительно привязки самой верхней фигуры на С#.
type: docs
weight: 80
url: /ru/net/aspose.words.drawing/shapebase/boundsinpoints/
---
## ShapeBase.BoundsInPoints property

Получает местоположение и размер содержащего блока фигуры в точках относительно привязки самой верхней фигуры.

```csharp
public RectangleF BoundsInPoints { get; }
```

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

### Смотрите также

* class [ShapeBase](../)
* пространство имен [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* сборка [Aspose.Words](../../../)
