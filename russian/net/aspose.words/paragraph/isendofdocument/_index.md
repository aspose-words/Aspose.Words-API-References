---
title: IsEndOfDocument
second_title: Справочник по API Aspose.Words для .NET
description: Истинно если этот абзац является последним абзацем в последнем разделе документа.
type: docs
weight: 60
url: /ru/net/aspose.words/paragraph/isendofdocument/
---
## Paragraph.IsEndOfDocument property

Истинно, если этот абзац является последним абзацем в последнем разделе документа.

```csharp
public bool IsEndOfDocument { get; }
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
// и затем начинает новую строку, добавляя новый абзац.
builder.Writeln("Hello world!");

Assert.True(builder.CurrentParagraph.IsEndOfDocument);
```

### Смотрите также

* class [Paragraph](../../paragraph)
* пространство имен [Aspose.Words](../../paragraph)
* сборка [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->