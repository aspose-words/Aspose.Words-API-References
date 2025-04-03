---
title: PageSetup.endnoteOptions property
linktitle: endnoteOptions property
articleTitle: endnoteOptions property
second_title: Aspose.Words for NodeJs
description: "PageSetup.endnoteOptions property. Provides options that control numbering and positioning of endnotes in this section."
type: docs
weight: 120
url: /nodejs-net/aspose.words/pagesetup/endnoteOptions/
---

## PageSetup.endnoteOptions property

Provides options that control numbering and positioning of endnotes in this section.


```js
get endnoteOptions(): Aspose.Words.Notes.EndnoteOptions
```

### Examples

Shows how to configure options affecting footnotes/endnotes in a section.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

builder.write("Hello world!");
builder.insertFootnote(aw.Notes.FootnoteType.Footnote, "Footnote reference text.");

// Configure all footnotes in the first section to restart the numbering from 1
// at each new page and display themselves directly beneath the text on every page.
let footnoteOptions = doc.sections.at(0).pageSetup.footnoteOptions;
footnoteOptions.position = aw.Notes.FootnotePosition.BeneathText;
footnoteOptions.restartRule = aw.Notes.FootnoteNumberingRule.RestartPage;
footnoteOptions.startNumber = 1;

builder.write(" Hello again.");
builder.insertFootnote(aw.Notes.FootnoteType.Footnote, "Endnote reference text.");

// Configure all endnotes in the first section to maintain a continuous count throughout the section,
// starting from 1. Also, set them all to appear collected at the end of the document.
let endnoteOptions = doc.sections.at(0).pageSetup.endnoteOptions;
endnoteOptions.position = aw.Notes.EndnotePosition.EndOfDocument;
endnoteOptions.restartRule = aw.Notes.FootnoteNumberingRule.Continuous;
endnoteOptions.startNumber = 1;

doc.save(base.artifactsDir + "PageSetup.footnoteOptions.docx");
```

### See Also

* module [Aspose.Words](../../)
* class [PageSetup](../)

