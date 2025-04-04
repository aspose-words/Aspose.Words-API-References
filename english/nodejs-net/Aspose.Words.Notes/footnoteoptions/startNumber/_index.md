---
title: FootnoteOptions.startNumber property
linktitle: startNumber property
articleTitle: startNumber property
second_title: Aspose.Words for Node.js
description: "FootnoteOptions.startNumber property. Specifies the starting number or character for the first automatically numbered footnotes."
type: docs
weight: 50
url: /nodejs-net/aspose.words.notes/footnoteoptions/startNumber/
---

## FootnoteOptions.startNumber property

Specifies the starting number or character for the first automatically numbered footnotes.


```js
get startNumber(): number
```

### Remarks

This property has effect only when [FootnoteOptions.restartRule](../restartRule/) is set to
[FootnoteNumberingRule.Continuous](../../footnotenumberingrule/#Continuous).




### Examples

Shows how to set a number at which the document begins the footnote/endnote count.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

// Footnotes and endnotes are a way to attach a reference or a side comment to text
// that does not interfere with the main body text's flow. 
// Inserting a footnote/endnote adds a small superscript reference symbol
// at the main body text where we insert the footnote/endnote.
// Each footnote/endnote also creates an entry, which consists of a symbol
// that matches the reference symbol in the main body text.
// The reference text that we pass to the document builder's "InsertEndnote" method.
// Footnote entries, by default, show up at the bottom of each page that contains
// their reference symbols, and endnotes show up at the end of the document.
builder.write("Text 1. ");
builder.insertFootnote(aw.Notes.FootnoteType.Footnote, "Footnote 1.");
builder.write("Text 2. ");
builder.insertFootnote(aw.Notes.FootnoteType.Footnote, "Footnote 2.");
builder.write("Text 3. ");
builder.insertFootnote(aw.Notes.FootnoteType.Footnote, "Footnote 3.");

builder.insertParagraph();

builder.write("Text 1. ");
builder.insertFootnote(aw.Notes.FootnoteType.Endnote, "Endnote 1.");
builder.write("Text 2. ");
builder.insertFootnote(aw.Notes.FootnoteType.Endnote, "Endnote 2.");
builder.write("Text 3. ");
builder.insertFootnote(aw.Notes.FootnoteType.Endnote, "Endnote 3.");

// By default, the reference symbol for each footnote and endnote is its index
// among all the document's footnotes/endnotes. Each document maintains separate counts
// for footnotes and for endnotes, which both begin at 1.
expect(doc.footnoteOptions.startNumber).toEqual(1);
expect(doc.endnoteOptions.startNumber).toEqual(1);

// We can use the "StartNumber" property to get the document to
// begin a footnote or endnote count at a different number.
doc.endnoteOptions.numberStyle = aw.NumberStyle.Arabic;
doc.endnoteOptions.startNumber = 50;

doc.save(base.artifactsDir + "InlineStory.startNumber.docx");
```

### See Also

* module [Aspose.Words.Notes](../../)
* class [FootnoteOptions](../)

