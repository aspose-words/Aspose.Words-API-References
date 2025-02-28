---
title: ParagraphFormat.KeepTogether
linktitle: KeepTogether
articleTitle: KeepTogether
second_title: Aspose.Words for .NET
description: Discover the ParagraphFormat KeepTogether property: ensure all lines stay together on one page for improved document readability and professional presentation.
type: docs
weight: 160
url: /net/aspose.words/paragraphformat/keeptogether/
---
## ParagraphFormat.KeepTogether property

True if all lines in the paragraph are to remain on the same page.

```csharp
public bool KeepTogether { get; set; }
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

* class [ParagraphFormat](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
