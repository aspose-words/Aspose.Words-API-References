---
title: FootnoteType enumeration
linktitle: FootnoteType enumeration
articleTitle: FootnoteType enumeration
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.Notes.FootnoteType enumeration. Specifies whether this is a footnote or an endnote."
type: docs
weight: 100
url: /nodejs-net/aspose.words.notes/footnotetype/
---

## FootnoteType enumeration

Specifies whether this is a footnote or an endnote.

Both footnotes and endnotes are represented by objects by the [FootnoteType.Footnote](./#Footnote)
class. Use [Footnote.footnoteType](../footnote/footnoteType/) to distinguish between footnotes 
and endnotes.




### Members

| Name | Description |
| --- | --- |
| Footnote | The object is a footnote. |
| Endnote | The object is an endnote. |

### Examples

Shows how to reference text with a footnote and an endnote.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

// Insert some text and mark it with a footnote with the IsAuto property set to "true" by default,
// so the marker seen in the body text will be auto-numbered at "1",
// and the footnote will appear at the bottom of the page.
builder.write("This text will be referenced by a footnote.");
builder.insertFootnote(aw.Notes.FootnoteType.Footnote, "Footnote comment regarding referenced text.");

// Insert more text and mark it with an endnote with a custom reference mark,
// which will be used in place of the number "2" and set "IsAuto" to false.
builder.write("This text will be referenced by an endnote.");
builder.insertFootnote(aw.Notes.FootnoteType.Endnote, "Endnote comment regarding referenced text.", "CustomMark");

// Footnotes always appear at the bottom of their referenced text,
// so this page break will not affect the footnote.
// On the other hand, endnotes are always at the end of the document
// so that this page break will push the endnote down to the next page.
builder.insertBreak(aw.BreakType.PageBreak);

doc.save(base.artifactsDir + "DocumentBuilder.insertFootnote.docx");
```

Shows how to insert and customize footnotes.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

// Add text, and reference it with a footnote. This footnote will place a small superscript reference
// mark after the text that it references and create an entry below the main body text at the bottom of the page.
// This entry will contain the footnote's reference mark and the reference text,
// which we will pass to the document builder's "InsertFootnote" method.
builder.write("Main body text.");
let footnote = builder.insertFootnote(aw.Notes.FootnoteType.Footnote, "Footnote text.");

// If this property is set to "true", then our footnote's reference mark
// will be its index among all the section's footnotes.
// This is the first footnote, so the reference mark will be "1".
expect(footnote.isAuto).toEqual(true);

// We can move the document builder inside the footnote to edit its reference text. 
builder.moveTo(footnote.firstParagraph);
builder.write(" More text added by a DocumentBuilder.");
builder.moveToDocumentEnd();

expect(footnote.getText().trim()).toEqual("\u0002 Footnote text. More text added by a DocumentBuilder.");

builder.write(" More main body text.");
footnote = builder.insertFootnote(aw.Notes.FootnoteType.Footnote, "Footnote text.");

// We can set a custom reference mark which the footnote will use instead of its index number.
footnote.referenceMark = "RefMark";

expect(footnote.isAuto).toEqual(false);

// A bookmark with the "IsAuto" flag set to true will still show its real index
// even if previous bookmarks display custom reference marks, so this bookmark's reference mark will be a "3".
builder.write(" More main body text.");
footnote = builder.insertFootnote(aw.Notes.FootnoteType.Footnote, "Footnote text.");

expect(footnote.isAuto).toEqual(true);

doc.save(base.artifactsDir + "InlineStory.AddFootnote.docx");
```

### See Also

* module [Aspose.Words.Notes](../)
* enum value [FootnoteType.Footnote](./#Footnote)

