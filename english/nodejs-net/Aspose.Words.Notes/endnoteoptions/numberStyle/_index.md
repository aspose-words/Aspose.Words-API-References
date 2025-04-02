---
title: EndnoteOptions.numberStyle property
linktitle: numberStyle property
articleTitle: numberStyle property
second_title: Aspose.Words for NodeJs
description: "EndnoteOptions.numberStyle property. Specifies the number format for automatically numbered endnotes."
type: docs
weight: 10
url: /nodejs-net/Aspose.Words.Notes/endnoteoptions/numberStyle/
---

## EndnoteOptions.numberStyle property

Specifies the number format for automatically numbered endnotes.


```js
get numberStyle(): Aspose.Words.NumberStyle
```

### Remarks

Not all number styles are applicable for this property. For the list of applicable
number styles see the Insert Footnote or Endnote dialog box in Microsoft Word. If you select
a number style that is not applicable, Microsoft Word will revert to a default value.




### Examples

Shows how to change the number style of footnote/endnote reference marks.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

// Footnotes and endnotes are a way to attach a reference or a side comment to text
// that does not interfere with the main body text's flow. 
// Inserting a footnote/endnote adds a small superscript reference symbol
// at the main body text where we insert the footnote/endnote.
// Each footnote/endnote also creates an entry, which consists of a symbol that matches the reference
// symbol in the main body text. The reference text that we pass to the document builder's "InsertEndnote" method.
// Footnote entries, by default, show up at the bottom of each page that contains
// their reference symbols, and endnotes show up at the end of the document.
builder.write("Text 1. ");
builder.insertFootnote(aw.Notes.FootnoteType.Footnote, "Footnote 1.");
builder.write("Text 2. ");
builder.insertFootnote(aw.Notes.FootnoteType.Footnote, "Footnote 2.");
builder.write("Text 3. ");
builder.insertFootnote(aw.Notes.FootnoteType.Footnote, "Footnote 3.", "Custom footnote reference mark");

builder.insertParagraph();

builder.write("Text 1. ");
builder.insertFootnote(aw.Notes.FootnoteType.Endnote, "Endnote 1.");
builder.write("Text 2. ");
builder.insertFootnote(aw.Notes.FootnoteType.Endnote, "Endnote 2.");
builder.write("Text 3. ");
builder.insertFootnote(aw.Notes.FootnoteType.Endnote, "Endnote 3.", "Custom endnote reference mark");

// By default, the reference symbol for each footnote and endnote is its index
// among all the document's footnotes/endnotes. Each document maintains separate counts
// for footnotes and for endnotes. By default, footnotes display their numbers using Arabic numerals,
// and endnotes display their numbers in lowercase Roman numerals.
expect(doc.footnoteOptions.numberStyle).toEqual(aw.NumberStyle.Arabic);
expect(doc.endnoteOptions.numberStyle).toEqual(aw.NumberStyle.LowercaseRoman);

// We can use the "NumberStyle" property to apply custom numbering styles to footnotes and endnotes.
// This will not affect footnotes/endnotes with custom reference marks.
doc.footnoteOptions.numberStyle = aw.NumberStyle.UppercaseRoman;
doc.endnoteOptions.numberStyle = aw.NumberStyle.UppercaseLetter;

doc.save(base.artifactsDir + "InlineStory.RefMarkNumberStyle.docx");
```

### See Also

* module [Aspose.Words.Notes](../../)
* class [EndnoteOptions](../)

