---
title: TextBox.TextBoxWrapMode
linktitle: TextBoxWrapMode
articleTitle: TextBoxWrapMode
second_title: Aspose.Words для .NET
description: Откройте для себя свойство TextBox WrapMode, которое позволяет улучшить обтекание текстом фигур, повышая ясность и визуальную привлекательность вашего дизайна.
type: docs
weight: 110
url: /ru/net/aspose.words.drawing/textbox/textboxwrapmode/
---
## TextBox.TextBoxWrapMode property

Определяет, как текст обтекает фигуру.

```csharp
public TextBoxWrapMode TextBoxWrapMode { get; set; }
```

## Примечания

Значение по умолчанию:Square.

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

* enum [TextBoxWrapMode](../../textboxwrapmode/)
* class [TextBox](../)
* пространство имен [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* сборка [Aspose.Words](../../../)
