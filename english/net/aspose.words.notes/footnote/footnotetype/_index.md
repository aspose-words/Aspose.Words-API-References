---
title: Footnote.FootnoteType
linktitle: FootnoteType
articleTitle: FootnoteType
second_title: Aspose.Words for .NET
description: Discover the FootnoteType property, easily identify footnotes or endnotes in your documents for enhanced clarity and organization.
type: docs
weight: 30
url: /net/aspose.words.notes/footnote/footnotetype/
---
## Footnote.FootnoteType property

Returns a value that specifies whether this is a footnote or endnote.

```csharp
public FootnoteType FootnoteType { get; }
```

## Examples

Shows the difference between footnotes and endnotes.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Below are two ways of attaching numbered references to the text. Both these references will add a
// small superscript reference mark at the location that we insert them.
// The reference mark, by default, is the index number of the reference among all the references in the document.
// Each reference will also create an entry, which will have the same reference mark as in the body text
// and reference text, which we will pass to the document builder's "InsertFootnote" method.
// 1 -  A footnote, whose entry will appear on the same page as the text that it references:
builder.Write("Footnote referenced main body text.");
Footnote footnote = builder.InsertFootnote(FootnoteType.Footnote, 
    "Footnote text, will appear at the bottom of the page that contains the referenced text.");

// 2 -  An endnote, whose entry will appear at the end of the document:
builder.Write("Endnote referenced main body text.");
Footnote endnote = builder.InsertFootnote(FootnoteType.Endnote, 
    "Endnote text, will appear at the very end of the document.");

builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.InsertBreak(BreakType.SectionBreakNewPage);

Assert.That(footnote.FootnoteType, Is.EqualTo(FootnoteType.Footnote));
Assert.That(endnote.FootnoteType, Is.EqualTo(FootnoteType.Endnote));

doc.Save(ArtifactsDir + "InlineStory.FootnoteEndnote.docx");
```

### See Also

* enum [FootnoteType](../../footnotetype/)
* class [Footnote](../)
* namespace [Aspose.Words.Notes](../../../aspose.words.notes/)
* assembly [Aspose.Words](../../../)
