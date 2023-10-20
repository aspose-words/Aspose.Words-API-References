---
title: ShapeBase.FlipOrientation
linktitle: FlipOrientation
articleTitle: FlipOrientation
second_title: Aspose.Words для .NET
description: ShapeBase FlipOrientation свойство. Переключает ориентацию фигуры на С#.
type: docs
weight: 180
url: /ru/net/aspose.words.drawing/shapebase/fliporientation/
---
## ShapeBase.FlipOrientation property

Переключает ориентацию фигуры.

```csharp
public FlipOrientation FlipOrientation { get; set; }
```

## Примечания

Значение по умолчанию:None.

## Примеры

Показывает, как перевернуть фигуру по оси.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Вставляем фигуру изображения и оставляем ее ориентацию в состоянии по умолчанию.
Shape shape = builder.InsertShape(ShapeType.Rectangle, RelativeHorizontalPosition.LeftMargin, 100,
    RelativeVerticalPosition.TopMargin, 100, 100, 100, WrapType.None);
shape.ImageData.SetImage(ImageDir + "Logo.jpg");

Assert.AreEqual(FlipOrientation.None, shape.FlipOrientation);

shape = builder.InsertShape(ShapeType.Rectangle, RelativeHorizontalPosition.LeftMargin, 250,
    RelativeVerticalPosition.TopMargin, 100, 100, 100, WrapType.None);
shape.ImageData.SetImage(ImageDir + "Logo.jpg");

// Установите для свойства «FlipOrientation» значение «FlipOrientation.Horizontal», чтобы перевернуть вторую фигуру по оси Y,
// превращаем ее в горизонтальное зеркальное отображение первой фигуры.
shape.FlipOrientation = FlipOrientation.Horizontal;

shape = builder.InsertShape(ShapeType.Rectangle, RelativeHorizontalPosition.LeftMargin, 100,
    RelativeVerticalPosition.TopMargin, 250, 100, 100, WrapType.None);
shape.ImageData.SetImage(ImageDir + "Logo.jpg");

// Установите для свойства «FlipOrientation» значение «FlipOrientation.Horizontal», чтобы перевернуть третью фигуру по оси X,
// превращаем ее в вертикальное зеркальное отображение первой фигуры.
shape.FlipOrientation = FlipOrientation.Vertical;

shape = builder.InsertShape(ShapeType.Rectangle, RelativeHorizontalPosition.LeftMargin, 250,
    RelativeVerticalPosition.TopMargin, 250, 100, 100, WrapType.None);
shape.ImageData.SetImage(ImageDir + "Logo.jpg");

// Установите для свойства «FlipOrientation» значение «FlipOrientation.Horizontal», чтобы перевернуть четвертую фигуру по осям X и Y,
// превращаем ее в горизонтальное и вертикальное зеркальное отображение первой фигуры.
shape.FlipOrientation = FlipOrientation.Both;

doc.Save(ArtifactsDir + "Shape.FlipShapeOrientation.docx");
```

### Смотрите также

* enum [FlipOrientation](../../fliporientation/)
* class [ShapeBase](../)
* пространство имен [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* сборка [Aspose.Words](../../../)
