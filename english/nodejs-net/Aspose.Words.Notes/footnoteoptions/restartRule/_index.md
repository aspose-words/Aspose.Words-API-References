---
title: FootnoteOptions.restartRule property
linktitle: restartRule property
articleTitle: restartRule property
second_title: Aspose.Words for Node.js
description: "FootnoteOptions.restartRule property. Determines when automatic numbering restarts."
type: docs
weight: 40
url: /nodejs-net/aspose.words.notes/footnoteoptions/restartRule/
---

## FootnoteOptions.restartRule property

Determines when automatic numbering restarts.


```js
get restartRule(): Aspose.Words.Notes.FootnoteNumberingRule
```

### Examples

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

### See Also

* module [Aspose.Words.Notes](../../)
* class [FootnoteOptions](../)

