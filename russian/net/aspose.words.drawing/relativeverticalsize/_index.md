---
title: RelativeVerticalSize Enum
linktitle: RelativeVerticalSize
articleTitle: RelativeVerticalSize
second_title: Aspose.Words для .NET
description: Откройте для себя перечисление Aspose.Words.Drawing.RelativeVerticalSize, которое определяет расчеты вертикальной высоты для фигур и текстовых фреймов, повышая точность макета документа.
type: docs
weight: 1610
url: /ru/net/aspose.words.drawing/relativeverticalsize/
---
## RelativeVerticalSize enumeration

Указывает, относительно чего вычисляется высота фигуры или текстовой рамки по вертикали.

```csharp
public enum RelativeVerticalSize
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| Margin | `0` | Указывает, что высота рассчитывается относительно пространства между верхним и нижним полями. |
| Page | `1` | Указывает, что высота рассчитывается относительно высоты страницы. |
| TopMargin | `2` | Указывает, что высота рассчитывается относительно размера области верхнего поля. |
| BottomMargin | `3` | Указывает, что высота рассчитывается относительно размера области нижнего поля. |
| InnerMargin | `4` | Указывает, что высота рассчитывается относительно размера области внутреннего поля, относительно размера области верхнего поля для нечетных страниц и относительно размера области нижнего поля для четных страниц. |
| OuterMargin | `5` | Указывает, что высота рассчитывается относительно размера области внешнего поля, относительно размера области нижнего поля для нечетных страниц и относительно размера области верхнего поля для четных страниц. |
| Default | `1` | Значение по умолчанию:Margin . |

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

* property [RelativeVerticalSize](../shapebase/relativeverticalsize/)
* пространство имен [Aspose.Words.Drawing](../../aspose.words.drawing/)
* сборка [Aspose.Words](../../)
