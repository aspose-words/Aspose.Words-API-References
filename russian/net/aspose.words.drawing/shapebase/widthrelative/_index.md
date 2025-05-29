---
title: ShapeBase.WidthRelative
linktitle: WidthRelative
articleTitle: WidthRelative
second_title: Aspose.Words для .NET
description: Откройте для себя свойство ShapeBase WidthRelative, позволяющее легко настраивать ширину фигур в процентах, повышая гибкость и точность вашего дизайна.
type: docs
weight: 620
url: /ru/net/aspose.words.drawing/shapebase/widthrelative/
---
## ShapeBase.WidthRelative property

Возвращает или задает значение, представляющее процент относительной ширины фигуры.

```csharp
public float WidthRelative { get; set; }
```

## Примеры

Показывает, как задать относительный размер и положение.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Добавляем простую фигуру с абсолютным размером и положением.
Shape shape = builder.InsertShape(ShapeType.Rectangle, 100, 40);
// Установите WrapType на WrapType.None, поскольку встроенные фигуры автоматически преобразуются в абсолютные единицы.
shape.WrapType = WrapType.None;

// Проверка и установка относительного горизонтального размера.
if (shape.RelativeHorizontalSize == RelativeHorizontalSize.Default)
{
    // Устанавливаем привязку горизонтального размера к Margin.
    shape.RelativeHorizontalSize = RelativeHorizontalSize.Margin;
    // Устанавливаем ширину 50% от ширины поля.
    shape.WidthRelative = 50;
}

// Проверка и установка относительного вертикального размера.
if (shape.RelativeVerticalSize == RelativeVerticalSize.Default)
{
    // Устанавливаем привязку вертикального размера к Margin.
    shape.RelativeVerticalSize = RelativeVerticalSize.Margin;
    // Устанавливаем высоту 30% от высоты поля.
    shape.HeightRelative = 30;
}

// Проверка и установка относительного вертикального положения.
if (shape.RelativeVerticalPosition == RelativeVerticalPosition.Paragraph)
{
    // установка привязки позиции к TopMargin.
    shape.RelativeVerticalPosition = RelativeVerticalPosition.TopMargin;
    // Установка относительного верха на 30% от позиции TopMargin.
    shape.TopRelative = 30;
}

// Проверка и установка относительного горизонтального положения.
if (shape.RelativeHorizontalPosition == RelativeHorizontalPosition.Default)
{
    // Устанавливаем привязку позиции к RightMargin.
    shape.RelativeHorizontalPosition = RelativeHorizontalPosition.RightMargin;
    // Относительное значение позиции может быть отрицательным.
    shape.LeftRelative = -260;
}

doc.Save(ArtifactsDir + "Shape.RelativeSizeAndPosition.docx");
```

### Смотрите также

* class [ShapeBase](../)
* пространство имен [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* сборка [Aspose.Words](../../../)
