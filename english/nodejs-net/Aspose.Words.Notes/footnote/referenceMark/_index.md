---
title: Footnote.referenceMark property
linktitle: referenceMark property
articleTitle: referenceMark property
second_title: Aspose.Words for NodeJs
description: "Footnote.referenceMark property. Gets/sets custom reference mark to be used for this footnote"
type: docs
weight: 60
url: /nodejs-net/Aspose.Words.Notes/footnote/referenceMark/
---

## Footnote.referenceMark property

Gets/sets custom reference mark to be used for this footnote.
Default value is **empty string** (), meaning auto-numbered footnotes are used.



```js
get referenceMark(): string
```

### Remarks

If this property is set to **empty string** () or ``null``, then [Footnote.isAuto](../isAuto/) property will automatically be set to ``true``, 
if set to anything else then [Footnote.isAuto](../isAuto/) will be set to ``false``.


RTF-format can only store 1 symbol as custom reference mark, so upon export only the first symbol will be written others will be discard.




### Examples

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

* module [Aspose.Words.Notes](../../)
* class [Footnote](../)

