---
title: ShapeBase.HeightRelative
linktitle: HeightRelative
articleTitle: HeightRelative
second_title: Aspose.Words для .NET
description: ShapeBase HeightRelative свойство. Получает или задает значение представляющее процент относительной высоты фигуры на С#.
type: docs
weight: 210
url: /ru/net/aspose.words.drawing/shapebase/heightrelative/
---
## ShapeBase.HeightRelative property

Получает или задает значение, представляющее процент относительной высоты фигуры.

```csharp
public float HeightRelative { get; set; }
```

## Примеры

Показывает, как установить относительный размер и положение.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Добавляем простую фигуру с абсолютным размером и положением.
Shape shape = builder.InsertShape(ShapeType.Rectangle, 100, 40);
// Установите для WrapType значение WrapType.None, поскольку встроенные фигуры автоматически преобразуются в абсолютные единицы.
shape.WrapType = WrapType.None;

// Проверка и установка относительного размера по горизонтали.
if (shape.RelativeHorizontalSize == RelativeHorizontalSize.Default)
{
    // Установка привязки горизонтального размера к Margin.
    shape.RelativeHorizontalSize = RelativeHorizontalSize.Margin;
    // Установка ширины 50% от ширины поля.
    shape.WidthRelative = 50;
}

// Проверка и установка относительного размера по вертикали.
if (shape.RelativeVerticalSize == RelativeVerticalSize.Default)
{
    // Установка привязки вертикального размера к Margin.
    shape.RelativeVerticalSize = RelativeVerticalSize.Margin;
    // Установка высоты 30% от высоты поля.
    shape.HeightRelative = 30;
}

// Проверка и установка относительного вертикального положения.
if (shape.RelativeVerticalPosition == RelativeVerticalPosition.Paragraph)
{
    // установка привязки позиции к TopMargin.
    shape.RelativeVerticalPosition = RelativeVerticalPosition.TopMargin;
    // Установка относительного Top на 30% от позиции TopMargin.
    shape.TopRelative = 30;
}

// Проверка и установка относительного горизонтального положения.
if (shape.RelativeHorizontalPosition == RelativeHorizontalPosition.Default)
{
    // Установка привязки позиции к RightMargin.
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
