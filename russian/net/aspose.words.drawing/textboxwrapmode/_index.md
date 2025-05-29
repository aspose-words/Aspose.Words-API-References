---
title: TextBoxWrapMode Enum
linktitle: TextBoxWrapMode
articleTitle: TextBoxWrapMode
second_title: Aspose.Words для .NET
description: Откройте для себя перечисление Aspose.Words.Drawing.TextBoxWrapMode для управления обтеканием текстом фигур, улучшения макетов документов и гибкости дизайна.
type: docs
weight: 1750
url: /ru/net/aspose.words.drawing/textboxwrapmode/
---
## TextBoxWrapMode enumeration

Указывает, как текст обтекает фигуру.

```csharp
public enum TextBoxWrapMode
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| Square | `0` | Текст обтекает фигуру. |
| None | `2` | Текст не переносится внутри фигуры. |

## Примеры

Показывает, как установить режим обтекания для содержимого текстового поля.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape textBoxShape = builder.InsertShape(ShapeType.TextBox, 300, 300);
TextBox textBox = textBoxShape.TextBox;

// Установите свойство "TextBoxWrapMode" на "TextBoxWrapMode.None", чтобы увеличить ширину текстового поля
// для размещения текста, если он достаточно большой.
// Установите свойство "TextBoxWrapMode" на "TextBoxWrapMode.Square" для
// обернуть весь текст внутри текстового поля, сохранив его размеры.
textBox.TextBoxWrapMode = textBoxWrapMode;

builder.MoveTo(textBoxShape.LastParagraph);
builder.Font.Size = 32;
builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

doc.Save(ArtifactsDir + "Shape.TextBoxContentsWrapMode.docx");
```

### Смотрите также

* пространство имен [Aspose.Words.Drawing](../../aspose.words.drawing/)
* сборка [Aspose.Words](../../)
