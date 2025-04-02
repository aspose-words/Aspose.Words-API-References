---
title: PageSetup.sheetsPerBooklet property
linktitle: sheetsPerBooklet property
articleTitle: sheetsPerBooklet property
second_title: Aspose.Words for NodeJs
description: "PageSetup.sheetsPerBooklet property. Returns or sets the number of pages to be included in each booklet."
type: docs
weight: 400
url: /nodejs-net/Aspose.Words/pagesetup/sheetsPerBooklet/
---

## PageSetup.sheetsPerBooklet property

Returns or sets the number of pages to be included in each booklet.


```js
get sheetsPerBooklet(): number
```

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

* module [Aspose.Words](../../)
* class [PageSetup](../)

