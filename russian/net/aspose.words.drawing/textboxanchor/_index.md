---
title: TextBoxAnchor Enum
linktitle: TextBoxAnchor
articleTitle: TextBoxAnchor
second_title: Aspose.Words для .NET
description: Aspose.Words.Drawing.TextBoxAnchor перечисление. Указывает значения используемые для вертикального выравнивания текста фигуры на С#.
type: docs
weight: 1330
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
| Bottom | `2` | Текст выравнивается по нижней части текстового поля. |
| TopCentered | `3` | Текст выравнивается по центру верхнего края текстового поля. |
| MiddleCentered | `4` | Текст выравнивается по центру текстового поля. |
| BottomCentered | `5` | Текст выравнивается по нижнему центру текстового поля. |
| TopBaseline | `6` | Текст выравнивается по верхней базовой линии текстового поля. |
| BottomBaseline | `7` | Текст выравнивается по нижней базовой линии текстового поля. |
| TopCenteredBaseline | `8` | Текст выравнивается по центральной верхней базовой линии текстового поля. |
| BottomCenteredBaseline | `9` | Текст выравнивается по нижней центральной базовой линии текстового поля. |

## Примеры

Показывает, как выровнять текстовое содержимое текстового поля по вертикали.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.TextBox, 200, 200);

// Установите для свойства "VerticalAnchor" значение "TextBoxAnchor.Top", чтобы
// выравниваем текст в этом текстовом поле по верхней стороне фигуры.
// Установите для свойства "VerticalAnchor" значение "TextBoxAnchor.Middle", чтобы
// выравниваем текст в этом текстовом поле по центру фигуры.
// Установите для свойства "VerticalAnchor" значение "TextBoxAnchor.Bottom", чтобы
// выравниваем текст в этом текстовом поле по низу фигуры.
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
