---
title: MultiplePagesType enumeration
linktitle: MultiplePagesType enumeration
articleTitle: MultiplePagesType enumeration
second_title: Aspose.Words for Node.js
description: "Aspose.Words.Settings.MultiplePagesType enumeration. Specifies how document is printed out."
type: docs
weight: 110
url: /nodejs-net/aspose.words.settings/multiplepagestype/
---

## MultiplePagesType enumeration

Specifies how document is printed out.


### Members

| Name | Description |
| --- | --- |
| Normal | Normal printing, no multiple pages specified. |
| MirrorMargins | Swaps left and right margins on facing pages. |
| TwoPagesPerSheet | Prints two pages per sheet. |
| BookFoldPrinting | Specifies whether to print the document as a book fold. |
| BookFoldPrintingReverse | Specifies whether to print the document as a reverse book fold. |
| Default | Default value is [MultiplePagesType.Normal](./#Normal) |

### Examples

Shows how to configure a document that can be printed as a book fold.

```js
let doc = new aw.Document();

// Insert text that spans 16 pages.
let builder = new aw.DocumentBuilder(doc);
builder.writeln("My Booklet:");

for (let i = 0; i < 15; i++)
{
  builder.insertBreak(aw.BreakType.PageBreak);
  builder.write(`Booklet face #${i}`);
}

// Configure the first section's "PageSetup" property to print the document in the form of a book fold.
// When we print this document on both sides, we can take the pages to stack them
// and fold them all down the middle at once. The contents of the document will line up into a book fold.
let pageSetup = doc.sections.at(0).pageSetup;
pageSetup.multiplePages = aw.Settings.MultiplePagesType.BookFoldPrinting;

// We can only specify the number of sheets in multiples of 4.
pageSetup.sheetsPerBooklet = 4;

doc.save(base.artifactsDir + "PageSetup.Booklet.docx");
```

### See Also

* module [Aspose.Words.Settings](../)

