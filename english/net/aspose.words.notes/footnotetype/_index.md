---
title: FootnoteType Enum
linktitle: FootnoteType
articleTitle: FootnoteType
second_title: Aspose.Words for .NET
description: Discover Aspose.Words.FootnoteType enum. Easily distinguish between footnotes and endnotes for enhanced document formatting and clarity.
type: docs
weight: 5010
url: /net/aspose.words.notes/footnotetype/
---
## FootnoteType enumeration

Specifies whether this is a footnote or an endnote.

```csharp
public enum FootnoteType
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Footnote | `0` | The object is a footnote. |
| Endnote | `1` | The object is an endnote. |

## Remarks

Both footnotes and endnotes are represented by objects by the Footnote class. Use [`FootnoteType`](../footnote/footnotetype/) to distinguish between footnotes and endnotes.

## Examples

Shows how to reference text with a footnote and an endnote.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insert some text and mark it with a footnote with the IsAuto property set to "true" by default,
// so the marker seen in the body text will be auto-numbered at "1",
// and the footnote will appear at the bottom of the page.
builder.Write("This text will be referenced by a footnote.");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote comment regarding referenced text.");

// Insert more text and mark it with an endnote with a custom reference mark,
// which will be used in place of the number "2" and set "IsAuto" to false.
builder.Write("This text will be referenced by an endnote.");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote comment regarding referenced text.", "CustomMark");

// Footnotes always appear at the bottom of their referenced text,
// so this page break will not affect the footnote.
// On the other hand, endnotes are always at the end of the document
// so that this page break will push the endnote down to the next page.
builder.InsertBreak(BreakType.PageBreak);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertFootnote.docx");
```

Shows how to insert and customize footnotes.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Add text, and reference it with a footnote. This footnote will place a small superscript reference
// mark after the text that it references and create an entry below the main body text at the bottom of the page.
// This entry will contain the footnote's reference mark and the reference text,
// which we will pass to the document builder's "InsertFootnote" method.
builder.Write("Main body text.");
Footnote footnote = builder.InsertFootnote(FootnoteType.Footnote, "Footnote text.");

// If this property is set to "true", then our footnote's reference mark
// will be its index among all the section's footnotes.
// This is the first footnote, so the reference mark will be "1".
Assert.That(footnote.IsAuto, Is.True);

// We can move the document builder inside the footnote to edit its reference text. 
builder.MoveTo(footnote.FirstParagraph);
builder.Write(" More text added by a DocumentBuilder.");
builder.MoveToDocumentEnd();

Assert.That(footnote.GetText().Trim(), Is.EqualTo("\u0002 Footnote text. More text added by a DocumentBuilder."));

builder.Write(" More main body text.");
footnote = builder.InsertFootnote(FootnoteType.Footnote, "Footnote text.");

// We can set a custom reference mark which the footnote will use instead of its index number.
footnote.ReferenceMark = "RefMark";

Assert.That(footnote.IsAuto, Is.False);

// A bookmark with the "IsAuto" flag set to true will still show its real index
// even if previous bookmarks display custom reference marks, so this bookmark's reference mark will be a "3".
builder.Write(" More main body text.");
footnote = builder.InsertFootnote(FootnoteType.Footnote, "Footnote text.");

Assert.That(footnote.IsAuto, Is.True);

doc.Save(ArtifactsDir + "InlineStory.AddFootnote.docx");
```

### See Also

* namespace [Aspose.Words.Notes](../../aspose.words.notes/)
* assembly [Aspose.Words](../../)
