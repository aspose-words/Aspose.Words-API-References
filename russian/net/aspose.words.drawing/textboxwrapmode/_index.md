---
title: TextBoxWrapMode Enum
linktitle: TextBoxWrapMode
articleTitle: TextBoxWrapMode
second_title: Aspose.Words для .NET
description: Aspose.Words.Drawing.TextBoxWrapMode перечисление. Указывает как текст переносится внутри фигуры на С#.
type: docs
weight: 1340
url: /ru/net/aspose.words.drawing/textboxwrapmode/
---
## TextBoxWrapMode enumeration

Указывает, как текст переносится внутри фигуры.

```csharp
public enum TextBoxWrapMode
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| Square | `0` | Текст переносится внутри фигуры. |
| None | `2` | Текст не переносится внутри фигуры. |

## Примеры

Показывает, как установить режим переноса содержимого текстового поля.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape textBoxShape = builder.InsertShape(ShapeType.TextBox, 300, 300);
TextBox textBox = textBoxShape.TextBox;

// Установите для свойства TextBoxWrapMode значение TextBoxWrapMode.None, чтобы увеличить ширину текстового поля.
// для размещения текста, если он достаточно большой.
// Установите для свойства TextBoxWrapMode значение TextBoxWrapMode.Square, чтобы
// переносим весь текст внутрь текстового поля, сохраняя его размеры.
textBox.TextBoxWrapMode = textBoxWrapMode;

builder.MoveTo(textBoxShape.LastParagraph);
builder.Font.Size = 32;
builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

doc.Save(ArtifactsDir + "Shape.TextBoxContentsWrapMode.docx");
```

### Смотрите также

* пространство имен [Aspose.Words.Drawing](../../aspose.words.drawing/)
* сборка [Aspose.Words](../../)
