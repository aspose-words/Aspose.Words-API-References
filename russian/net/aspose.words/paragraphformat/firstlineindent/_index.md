---
title: ParagraphFormat.FirstLineIndent
second_title: Справочник по API Aspose.Words для .NET
description: ParagraphFormat свойство. Получает или задает значение в пунктах для первой строки или выступающего отступа.
type: docs
weight: 120
url: /ru/net/aspose.words/paragraphformat/firstlineindent/
---
## ParagraphFormat.FirstLineIndent property

Получает или задает значение (в пунктах) для первой строки или выступающего отступа.

Используйте положительные значения, чтобы установить отступ первой строки, и отрицательные значения, чтобы установить выступающий отступ.

```csharp
public double FirstLineIndent { get; set; }
```

### Примеры

Показывает, как вставить абзац в документ.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Font font = builder.Font;
font.Size = 16;
font.Bold = true;
font.Color = Color.Blue;
font.Name = "Arial";
font.Underline = Underline.Dash;

ParagraphFormat paragraphFormat = builder.ParagraphFormat;
paragraphFormat.FirstLineIndent = 8;
paragraphFormat.Alignment = ParagraphAlignment.Justify;
paragraphFormat.AddSpaceBetweenFarEastAndAlpha = true;
paragraphFormat.AddSpaceBetweenFarEastAndDigit = true;
paragraphFormat.KeepTogether = true;

// Метод Writeln завершает абзац после добавления текста
// а затем начинается новая строка, добавляющая новый абзац.
builder.Writeln("Hello world!");

Assert.True(builder.CurrentParagraph.IsEndOfDocument);
```

### Смотрите также

* class [ParagraphFormat](../)
* пространство имен [Aspose.Words](../../paragraphformat/)
* сборка [Aspose.Words](../../../)


