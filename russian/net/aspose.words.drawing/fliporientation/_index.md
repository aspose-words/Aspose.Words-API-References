---
title: FlipOrientation Enum
linktitle: FlipOrientation
articleTitle: FlipOrientation
second_title: Aspose.Words для .NET
description: Откройте для себя перечисление Aspose.Words.Drawing.FlipOrientation для универсальных вариантов ориентации фигур. Улучшите дизайн вашего документа с помощью гибкой настройки!
type: docs
weight: 1290
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
| Horizontal | `1` | Перевернуть по оси Y, поменяв местами координаты X. |
| Vertical | `2` | Перевернуть по оси x, поменяв местами координаты y. |
| Both | `3` | Перевернуть по осям y и x. |

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

* property [FlipOrientation](../shapebase/fliporientation/)
* пространство имен [Aspose.Words.Drawing](../../aspose.words.drawing/)
* сборка [Aspose.Words](../../)
