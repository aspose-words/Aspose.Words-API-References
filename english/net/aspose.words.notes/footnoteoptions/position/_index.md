---
title: FootnoteOptions.Position
linktitle: Position
second_title: Aspose.Words for .NET API Reference
description: FootnoteOptions Position property. Specifies the footnotes position in C#.
type: docs
weight: 30
url: /net/aspose.words.notes/footnoteoptions/position/
---
## Position property

Specifies the footnotes position.

```csharp
public FootnotePosition Position { get; set; }
```

## Examples

Shows how to select a different place where the document collects and displays its footnotes.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// A footnote is a way to attach a reference or a side comment to text
// that does not interfere with the main body text's flow.  
// Inserting a footnote adds a small superscript reference symbol
// at the main body text where we insert the footnote.
// Each footnote also creates an entry at the bottom of the page, consisting of a symbol
// that matches the reference symbol in the main body text.
// The reference text that we pass to the document builder's "InsertFootnote" method.
builder.Write("Hello world!");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote contents.");

// We can use the "Position" property to determine where the document will place all its footnotes.
// If we set the value of the "Position" property to "FootnotePosition.BottomOfPage",
// every footnote will show up at the bottom of the page that contains its reference mark. This is the default value.
// If we set the value of the "Position" property to "FootnotePosition.BeneathText",
// every footnote will show up at the end of the page's text that contains its reference mark.
doc.FootnoteOptions.Position = footnotePosition;

doc.Save(ArtifactsDir + "InlineStory.PositionFootnote.docx");
```

### See Also

* enum [FootnotePosition](../../footnoteposition/)
* class [FootnoteOptions](../)
* namespace [Aspose.Words.Notes](../../footnoteoptions/)
* assembly [Aspose.Words](../../../)
