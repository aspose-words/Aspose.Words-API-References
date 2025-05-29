---
title: ShapeBase.RelativeVerticalSize
linktitle: RelativeVerticalSize
articleTitle: RelativeVerticalSize
second_title: Aspose.Words для .NET
description: Откройте для себя свойство ShapeBase RelativeVerticalSize, позволяющее легко настраивать вертикальные размеры фигур для повышения гибкости и точности проектирования.
type: docs
weight: 480
url: /ru/net/aspose.words.drawing/shapebase/relativeverticalsize/
---
## ShapeBase.RelativeVerticalSize property

Возвращает или задает значение относительного размера фигуры в вертикальном направлении.

```csharp
public RelativeVerticalSize RelativeVerticalSize { get; set; }
```

## Примечания

Значение по умолчанию:Margin.

Имеет эффект только если[`HeightRelative`](../heightrelative/) установлено.

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

* enum [RelativeVerticalSize](../../relativeverticalsize/)
* class [ShapeBase](../)
* пространство имен [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* сборка [Aspose.Words](../../../)
