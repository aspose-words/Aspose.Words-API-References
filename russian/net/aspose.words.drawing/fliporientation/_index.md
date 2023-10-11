---
title: Enum FlipOrientation
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.Drawing.FlipOrientation перечисление. Возможные значения ориентации фигуры.
type: docs
weight: 970
url: /ru/net/aspose.words.drawing/fliporientation/
---
## FlipOrientation enumeration

Возможные значения ориентации фигуры.

```csharp
[Flags]
public enum FlipOrientation
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| None | `0` | Координаты не перевернуты. |
| Horizontal | `1` | Перевернуть вдоль оси Y, поменяв координаты X на противоположные. |
| Vertical | `2` | Перевернуть вдоль оси X, изменив координаты Y. |
| Both | `3` | Перевернуть по осям Y и X. |

### Примеры

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

* property [FlipOrientation](../shapebase/fliporientation/)
* пространство имен [Aspose.Words.Drawing](../../aspose.words.drawing/)
* сборка [Aspose.Words](../../)


