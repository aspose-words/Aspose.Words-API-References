---
title: Paragraph.IsEndOfDocument
linktitle: IsEndOfDocument
articleTitle: IsEndOfDocument
second_title: Aspose.Words for .NET
description: Discover the IsEndOfDocument property for paragraphs. Learn how to identify the last paragraph in your document's final section for effective formatting.
type: docs
weight: 60
url: /net/aspose.words/paragraph/isendofdocument/
---
## Paragraph.IsEndOfDocument property

True if this paragraph is the last paragraph in the last section of the document.

```csharp
public bool IsEndOfDocument { get; }
```

## Examples

Shows how to insert a paragraph into the document.

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

// The "Writeln" method ends the paragraph after appending text
// and then starts a new line, adding a new paragraph.
builder.Writeln("Hello world!");

Assert.True(builder.CurrentParagraph.IsEndOfDocument);
```

### See Also

* class [Paragraph](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
