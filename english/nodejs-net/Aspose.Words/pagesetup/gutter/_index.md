---
title: PageSetup.gutter property
linktitle: gutter property
articleTitle: gutter property
second_title: Aspose.Words for NodeJs
description: "PageSetup.gutter property. Gets or sets the amount of extra space added to the margin for document binding."
type: docs
weight: 160
url: /nodejs-net/Aspose.Words/pagesetup/gutter/
---

## PageSetup.gutter property

Gets or sets the amount of extra space added to the margin for document binding.


```js
get gutter(): number
```

### Examples

Shows how to set gutter margins.

```js
let doc = new aw.Document();

// Insert text that spans several pages.
let builder = new aw.DocumentBuilder(doc);
for (let i = 0; i < 6; i++)
{
  builder.write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
        "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
  builder.insertBreak(aw.BreakType.PageBreak);
}

// A gutter adds whitespaces to either the left or right page margin,
// which makes up for the center folding of pages in a book encroaching on the page's layout.
let pageSetup = doc.sections.at(0).pageSetup;

// Determine how much space our pages have for text within the margins and then add an amount to pad a margin. 
expect(pageSetup.pageWidth - pageSetup.leftMargin - pageSetup.rightMargin).toEqual(468);

pageSetup.gutter = 100.0;

// Set the "RtlGutter" property to "true" to place the gutter in a more suitable position for right-to-left text.
pageSetup.rtlGutter = true;

// Set the "MultiplePages" property to "MultiplePagesType.MirrorMargins" to alternate
// the left/right page side position of margins every page.
pageSetup.multiplePages = aw.Settings.MultiplePagesType.MirrorMargins;

doc.save(base.artifactsDir + "PageSetup.gutter.docx");
```

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

