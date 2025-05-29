---
title: TextBoxAnchor Enum
linktitle: TextBoxAnchor
articleTitle: TextBoxAnchor
second_title: Aspose.Words для .NET
description: Откройте для себя перечисление Aspose.Words.Drawing.TextBoxAnchor для точного вертикального выравнивания текста формы. Улучшите форматирование документа без усилий!
type: docs
weight: 1740
url: /ru/net/aspose.words.drawing/textboxanchor/
---
## TextBoxAnchor enumeration

Указывает значения, используемые для вертикального выравнивания текста фигуры.

```csharp
public enum TextBoxAnchor
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| Top | `0` | Текст выравнивается по верхнему краю текстового поля. |
| Middle | `1` | Текст выравнивается по середине текстового поля. |
| Bottom | `2` | Текст выравнивается по нижнему краю текстового поля. |
| TopCentered | `3` | Текст выравнивается по верхнему краю текстового поля. |
| MiddleCentered | `4` | Текст выравнивается по центру текстового поля. |
| BottomCentered | `5` | Текст выравнивается по нижнему краю текстового поля по центру. |
| TopBaseline | `6` | Текст выравнивается по верхней базовой линии текстового поля. |
| BottomBaseline | `7` | Текст выравнивается по нижней базовой линии текстового поля. |
| TopCenteredBaseline | `8` | Текст выравнивается по верхней центральной базовой линии текстового поля. |
| BottomCenteredBaseline | `9` | Текст выравнивается по нижней центральной базовой линии текстового поля. |

## Примеры

Показывает, как выровнять текстовое содержимое текстового поля по вертикали.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.TextBox, 200, 200);

// Установите свойство "VerticalAnchor" на "TextBoxAnchor.Top" для
// выровнять текст в этом текстовом поле по верхней стороне фигуры.
// Установите свойство "VerticalAnchor" на "TextBoxAnchor.Middle" для
// выровнять текст в этом текстовом поле по центру фигуры.
// Установите свойство "VerticalAnchor" на "TextBoxAnchor.Bottom" для
// выровнять текст в этом текстовом поле по нижнему краю фигуры.
shape.TextBox.VerticalAnchor = verticalAnchor;

builder.MoveTo(shape.FirstParagraph);
builder.Write("Hello world!");

// Вертикальное выравнивание текста внутри текстовых полей доступно начиная с Microsoft Word 2007.
doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2007);
doc.Save(ArtifactsDir + "Shape.VerticalAnchor.docx");
```

### Смотрите также

* пространство имен [Aspose.Words.Drawing](../../aspose.words.drawing/)
* сборка [Aspose.Words](../../)
