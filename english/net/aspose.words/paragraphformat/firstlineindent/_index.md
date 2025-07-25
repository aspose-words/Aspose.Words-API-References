---
title: ParagraphFormat.FirstLineIndent
linktitle: FirstLineIndent
articleTitle: FirstLineIndent
second_title: Aspose.Words for .NET
description: Discover how to use the ParagraphFormat FirstLineIndent property to easily customize first line or hanging indents in your documents for improved readability.
type: docs
weight: 120
url: /net/aspose.words/paragraphformat/firstlineindent/
---
## ParagraphFormat.FirstLineIndent property

Gets or sets the value (in points) for a first line or hanging indent.

Use positive values to set the first-line indent, and negative values to set the hanging indent.

```csharp
public double FirstLineIndent { get; set; }
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

Assert.That(builder.CurrentParagraph.IsEndOfDocument, Is.True);
```

### See Also

* class [ParagraphFormat](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
