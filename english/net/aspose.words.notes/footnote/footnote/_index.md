---
title: Footnote
linktitle: Footnote
articleTitle: Footnote
second_title: Aspose.Words for .NET
description: Create engaging footnotes effortlessly with our Footnote Constructor. Enhance your content's clarity and professionalism in just a few clicks!
type: docs
weight: 10
url: /net/aspose.words.notes/footnote/footnote/
---
## Footnote constructor

Initializes an instance of the [`Footnote`](../) class.

```csharp
public Footnote(DocumentBase doc, FootnoteType footnoteType)
```

| Parameter | Type | Description |
| --- | --- | --- |
| doc | DocumentBase | The owner document. |
| footnoteType | FootnoteType | A [`FootnoteType`](../footnotetype/) value that specifies whether this is a footnote or endnote. |

## Remarks

When [`Footnote`](../) is created, it belongs to the specified document, but is not yet part of the document and [`ParentNode`](../../../aspose.words/node/parentnode/) is `null`.

To append [`Footnote`](../) to the document use[`InsertAfter`](../../../aspose.words/compositenode/insertafter/) or [`InsertBefore`](../../../aspose.words/compositenode/insertbefore/) on the paragraph where you want the footnote inserted.

## Examples

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

* class [DocumentBase](../../../aspose.words/documentbase/)
* enum [FootnoteType](../../footnotetype/)
* class [Footnote](../)
* namespace [Aspose.Words.Notes](../../../aspose.words.notes/)
* assembly [Aspose.Words](../../../)
