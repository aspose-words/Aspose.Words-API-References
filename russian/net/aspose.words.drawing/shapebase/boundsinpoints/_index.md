---
title: ShapeBase.BoundsInPoints
linktitle: BoundsInPoints
articleTitle: BoundsInPoints
second_title: Aspose.Words для .NET
description: Откройте для себя свойство ShapeBase BoundsInPoints, которое позволяет легко получить доступ к размеру и местоположению фигуры в точках, повышая точность проектирования и контроль над макетом.
type: docs
weight: 80
url: /ru/net/aspose.words.drawing/shapebase/boundsinpoints/
---
## ShapeBase.BoundsInPoints property

Получает местоположение и размер содержащего блока фигуры в пунктах относительно точки привязки самой верхней фигуры.

```csharp
public RectangleF BoundsInPoints { get; }
```

## Примечания

Возвращаемые границы не включают поворот этой фигуры или поворот фигуры родительской группы, если таковой имеется.

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

### Смотрите также

* class [ShapeBase](../)
* пространство имен [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* сборка [Aspose.Words](../../../)
