---
title: ShapeBase.FlipOrientation
second_title: Справочник по API Aspose.Words для .NET
description: ShapeBase свойство. Переключает ориентацию фигуры.
type: docs
weight: 180
url: /ru/net/aspose.words.drawing/shapebase/fliporientation/
---
## ShapeBase.FlipOrientation property

Переключает ориентацию фигуры.

```csharp
public FlipOrientation FlipOrientation { get; set; }
```

### Примечания

Значение по умолчаниюNone.

### Примеры

Показывает, как отразить фигуру на оси.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Вставьте фигуру изображения и оставьте ее ориентацию в состоянии по умолчанию.
Shape shape = builder.InsertShape(ShapeType.Rectangle, RelativeHorizontalPosition.LeftMargin, 100,
    RelativeVerticalPosition.TopMargin, 100, 100, 100, WrapType.None);
shape.ImageData.SetImage(ImageDir + "Logo.jpg");

Assert.AreEqual(FlipOrientation.None, shape.FlipOrientation);

shape = builder.InsertShape(ShapeType.Rectangle, RelativeHorizontalPosition.LeftMargin, 250,
    RelativeVerticalPosition.TopMargin, 100, 100, 100, WrapType.None);
shape.ImageData.SetImage(ImageDir + "Logo.jpg");

// Установите для свойства "FlipOrientation" значение "FlipOrientation.Horizontal", чтобы отразить вторую фигуру по оси Y,
// превращаем его в горизонтальное зеркальное отображение первой формы.
shape.FlipOrientation = FlipOrientation.Horizontal;

shape = builder.InsertShape(ShapeType.Rectangle, RelativeHorizontalPosition.LeftMargin, 100,
    RelativeVerticalPosition.TopMargin, 250, 100, 100, WrapType.None);
shape.ImageData.SetImage(ImageDir + "Logo.jpg");

// Установите для свойства "FlipOrientation" значение "FlipOrientation.Horizontal", чтобы перевернуть третью фигуру по оси X,
// превращаем его в вертикальное зеркальное отображение первой формы.
shape.FlipOrientation = FlipOrientation.Vertical;

shape = builder.InsertShape(ShapeType.Rectangle, RelativeHorizontalPosition.LeftMargin, 250,
    RelativeVerticalPosition.TopMargin, 250, 100, 100, WrapType.None);
shape.ImageData.SetImage(ImageDir + "Logo.jpg");

// Установите для свойства "FlipOrientation" значение "FlipOrientation.Horizontal", чтобы отразить четвертую фигуру по обеим осям x и y,
// превращаем его в горизонтальное и вертикальное зеркальное отображение первой фигуры.
shape.FlipOrientation = FlipOrientation.Both;

doc.Save(ArtifactsDir + "Shape.FlipShapeOrientation.docx");
```

### Смотрите также

* enum [FlipOrientation](../../fliporientation/)
* class [ShapeBase](../)
* пространство имен [Aspose.Words.Drawing](../../shapebase/)
* сборка [Aspose.Words](../../../)


