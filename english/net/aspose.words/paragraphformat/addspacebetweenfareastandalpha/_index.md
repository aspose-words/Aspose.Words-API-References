---
title: AddSpaceBetweenFarEastAndAlpha
second_title: Aspose.Words for .NET API Reference
description: ParagraphFormat property. Gets or sets a flag indicating whether intercharacter spacing is automatically adjusted between regions of Latin text and regions of East Asian text in the current paragraph in C#.
type: docs
weight: 10
url: /net/aspose.words/paragraphformat/addspacebetweenfareastandalpha/
---
## ParagraphFormat.AddSpaceBetweenFarEastAndAlpha property

Gets or sets a flag indicating whether inter-character spacing is automatically adjusted between regions of Latin text and regions of East Asian text in the current paragraph.

```csharp
public bool AddSpaceBetweenFarEastAndAlpha { get; set; }
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
* namespace [Aspose.Words](../../paragraphformat/)
* assembly [Aspose.Words](../../../)
