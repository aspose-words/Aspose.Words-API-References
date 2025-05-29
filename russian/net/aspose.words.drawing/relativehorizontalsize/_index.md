---
title: RelativeHorizontalSize Enum
linktitle: RelativeHorizontalSize
articleTitle: RelativeHorizontalSize
second_title: Aspose.Words для .NET
description: Откройте для себя перечисление Aspose.Words.Drawing.RelativeHorizontalSize для точного управления формой и шириной текстовых рамок в ваших документах. Улучшите свое форматирование сегодня!
type: docs
weight: 1590
url: /ru/net/aspose.words.drawing/relativehorizontalsize/
---
## RelativeHorizontalSize enumeration

Указывает, относительно чего рассчитывается ширина фигуры или текстовой рамки по горизонтали.

```csharp
public enum RelativeHorizontalSize
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| Margin | `0` | Указывает, что ширина рассчитывается относительно пространства между левым и правым полями. |
| Page | `1` | Указывает, что ширина рассчитывается относительно ширины страницы. |
| LeftMargin | `2` | Указывает, что ширина рассчитывается относительно размера области левого поля. |
| RightMargin | `3` | Указывает, что ширина рассчитывается относительно размера области правого поля. |
| InnerMargin | `4` | Указывает, что ширина рассчитывается относительно размера области внутреннего поля, относительно размера области левого поля для нечетных страниц и относительно размера области правого поля для четных страниц. |
| OuterMargin | `5` | Указывает, что ширина рассчитывается относительно размера области внешнего поля, относительно размера области правого поля для нечетных страниц и относительно размера области левого поля для четных страниц. |
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

* property [RelativeHorizontalSize](../shapebase/relativehorizontalsize/)
* пространство имен [Aspose.Words.Drawing](../../aspose.words.drawing/)
* сборка [Aspose.Words](../../)
