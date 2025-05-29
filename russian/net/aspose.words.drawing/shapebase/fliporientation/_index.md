---
title: ShapeBase.FlipOrientation
linktitle: FlipOrientation
articleTitle: FlipOrientation
second_title: Aspose.Words для .NET
description: Откройте для себя свойство ShapeBase FlipOrientation, позволяющее легко менять ориентацию фигуры, делая ваши проекты более простыми и креативными.
type: docs
weight: 180
url: /ru/net/aspose.words.drawing/shapebase/fliporientation/
---
## ShapeBase.FlipOrientation property

Изменяет ориентацию фигуры.

```csharp
public FlipOrientation FlipOrientation { get; set; }
```

## Примечания

Значение по умолчанию:None.

## Примеры

Показывает, как перевернуть фигуру относительно оси.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Вставьте форму изображения и оставьте ее ориентацию в состоянии по умолчанию.
Shape shape = builder.InsertShape(ShapeType.Rectangle, RelativeHorizontalPosition.LeftMargin, 100,
    RelativeVerticalPosition.TopMargin, 100, 100, 100, WrapType.None);
shape.ImageData.SetImage(ImageDir + "Logo.jpg");

Assert.AreEqual(FlipOrientation.None, shape.FlipOrientation);

shape = builder.InsertShape(ShapeType.Rectangle, RelativeHorizontalPosition.LeftMargin, 250,
    RelativeVerticalPosition.TopMargin, 100, 100, 100, WrapType.None);
shape.ImageData.SetImage(ImageDir + "Logo.jpg");

// Установите свойство "FlipOrientation" на "FlipOrientation.Horizontal", чтобы перевернуть вторую фигуру по оси Y,
// превращая его в горизонтальное зеркальное отражение первой фигуры.
shape.FlipOrientation = FlipOrientation.Horizontal;

shape = builder.InsertShape(ShapeType.Rectangle, RelativeHorizontalPosition.LeftMargin, 100,
    RelativeVerticalPosition.TopMargin, 250, 100, 100, WrapType.None);
shape.ImageData.SetImage(ImageDir + "Logo.jpg");

// Установите свойство "FlipOrientation" на "FlipOrientation.Horizontal", чтобы перевернуть третью фигуру по оси x,
// превращая его в вертикальное зеркальное отражение первой фигуры.
shape.FlipOrientation = FlipOrientation.Vertical;

shape = builder.InsertShape(ShapeType.Rectangle, RelativeHorizontalPosition.LeftMargin, 250,
    RelativeVerticalPosition.TopMargin, 250, 100, 100, WrapType.None);
shape.ImageData.SetImage(ImageDir + "Logo.jpg");

// Установите свойство "FlipOrientation" на "FlipOrientation.Horizontal", чтобы перевернуть четвертую фигуру по осям x и y,
// превращая его в горизонтальное и вертикальное зеркальное отражение первой фигуры.
shape.FlipOrientation = FlipOrientation.Both;

doc.Save(ArtifactsDir + "Shape.FlipShapeOrientation.docx");
```

### Смотрите также

* enum [FlipOrientation](../../fliporientation/)
* class [ShapeBase](../)
* пространство имен [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* сборка [Aspose.Words](../../../)
