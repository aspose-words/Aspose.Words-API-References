---
title: Paragraph.IsEndOfDocument
linktitle: IsEndOfDocument
articleTitle: IsEndOfDocument
second_title: Aspose.Words для .NET
description: Откройте для себя свойство IsEndOfDocument для абзацев. Узнайте, как определить последний абзац в заключительном разделе документа для эффективного форматирования.
type: docs
weight: 60
url: /ru/net/aspose.words/paragraph/isendofdocument/
---
## Paragraph.IsEndOfDocument property

Истина, если этот абзац является последним абзацем в последнем разделе документа.

```csharp
public bool IsEndOfDocument { get; }
```

## Примеры

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
// а затем начинает новую строку, добавляя новый абзац.
builder.Writeln("Hello world!");

Assert.True(builder.CurrentParagraph.IsEndOfDocument);
```

### Смотрите также

* class [Paragraph](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
