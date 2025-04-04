---
title: FootnoteOptions class
linktitle: FootnoteOptions class
articleTitle: FootnoteOptions class
second_title: Aspose.Words for Node.js
description: "Aspose.Words.Notes.FootnoteOptions class. Represents the footnote numbering options for a document or section"
type: docs
weight: 50
url: /nodejs-net/aspose.words.notes/footnoteoptions/
---

## FootnoteOptions class

Represents the footnote numbering options for a document or section.
To learn more, visit the [Working with Footnote and Endnote](https://docs.aspose.com/words/nodejs-net/working-with-footnote-and-endnote/) documentation article.




### Properties

| Name | Description |
| --- | --- |
| [columns](./columns/) | Specifies the number of columns with which the footnotes area is formatted. |
| [numberStyle](./numberStyle/) | Specifies the number format for automatically numbered footnotes. |
| [position](./position/) | Specifies the footnotes position. |
| [restartRule](./restartRule/) | Determines when automatic numbering restarts. |
| [startNumber](./startNumber/) | Specifies the starting number or character for the first automatically numbered footnotes. |

### Examples

Shows how to select a different place where the document collects and displays its footnotes.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

// A footnote is a way to attach a reference or a side comment to text
// that does not interfere with the main body text's flow.  
// Inserting a footnote adds a small superscript reference symbol
// at the main body text where we insert the footnote.
// Each footnote also creates an entry at the bottom of the page, consisting of a symbol
// that matches the reference symbol in the main body text.
// The reference text that we pass to the document builder's "InsertFootnote" method.
builder.write("Hello world!");
builder.insertFootnote(aw.Notes.FootnoteType.Footnote, "Footnote contents.");

// We can use the "Position" property to determine where the document will place all its footnotes.
// If we set the value of the "Position" property to "FootnotePosition.BottomOfPage",
// every footnote will show up at the bottom of the page that contains its reference mark. This is the default value.
// If we set the value of the "Position" property to "FootnotePosition.BeneathText",
// every footnote will show up at the end of the page's text that contains its reference mark.
doc.footnoteOptions.position = footnotePosition;

doc.save(base.artifactsDir + "InlineStory.PositionFootnote.docx");
```

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

Shows how to restart footnote/endnote numbering at certain places in the document.

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
builder.insertBreak(aw.BreakType.PageBreak);
builder.write("Text 3. ");
builder.insertFootnote(aw.Notes.FootnoteType.Footnote, "Footnote 3.");
builder.write("Text 4. ");
builder.insertFootnote(aw.Notes.FootnoteType.Footnote, "Footnote 4.");

builder.insertBreak(aw.BreakType.PageBreak);

builder.write("Text 1. ");
builder.insertFootnote(aw.Notes.FootnoteType.Endnote, "Endnote 1.");
builder.write("Text 2. ");
builder.insertFootnote(aw.Notes.FootnoteType.Endnote, "Endnote 2.");
builder.insertBreak(aw.BreakType.SectionBreakNewPage);
builder.write("Text 3. ");
builder.insertFootnote(aw.Notes.FootnoteType.Endnote, "Endnote 3.");
builder.write("Text 4. ");
builder.insertFootnote(aw.Notes.FootnoteType.Endnote, "Endnote 4.");

// By default, the reference symbol for each footnote and endnote is its index
// among all the document's footnotes/endnotes. Each document maintains separate counts
// for footnotes and endnotes and does not restart these counts at any point.
expect(aw.Notes.FootnoteNumberingRule.Default).toEqual(doc.footnoteOptions.restartRule);
expect(aw.Notes.FootnoteNumberingRule.Continuous).toEqual(aw.Notes.FootnoteNumberingRule.Default);

// We can use the "RestartRule" property to get the document to restart
// the footnote/endnote counts at a new page or section.
doc.footnoteOptions.restartRule = aw.Notes.FootnoteNumberingRule.RestartPage;
doc.endnoteOptions.restartRule = aw.Notes.FootnoteNumberingRule.RestartSection;

doc.save(base.artifactsDir + "InlineStory.NumberingRule.docx");
```

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

* module [Aspose.Words.Notes](../)
* property [Document.footnoteOptions](../../aspose.words/document/footnoteOptions/)
* property [PageSetup.footnoteOptions](../../aspose.words/pagesetup/footnoteOptions/)

