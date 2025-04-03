---
title: FixedPageSaveOptions.pageSet property
linktitle: pageSet property
articleTitle: pageSet property
second_title: Aspose.Words for NodeJs
description: "FixedPageSaveOptions.pageSet property. Gets or sets the pages to render"
type: docs
weight: 70
url: /nodejs-net/Aspose.Words.Saving/fixedpagesaveoptions/pageSet/
---

## FixedPageSaveOptions.pageSet property

Gets or sets the pages to render.
Default is all the pages in the document.


```js
get pageSet(): Aspose.Words.Saving.PageSet
```

### Examples

Shows how to extract pages based on exact page indices.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

// Add five pages to the document.
for (let i = 1; i < 6; i++)
{
  builder.write("Page " + i);
  builder.insertBreak(aw.BreakType.PageBreak);
}

// Create an "XpsSaveOptions" object, which we can pass to the document's "Save" method
// to modify how that method converts the document to .XPS.
let xpsOptions = new aw.Saving.XpsSaveOptions();

// Use the "PageSet" property to select a set of the document's pages to save to output XPS.
// In this case, we will choose, via a zero-based index, only three pages: page 1, page 2, and page 4.
xpsOptions.pageSet = new aw.Saving.PageSet([0, 1, 3]);

doc.save(base.artifactsDir + "XpsSaveOptions.ExportExactPages.xps", xpsOptions);
```

Shows how to convert only some of the pages in a document to PDF.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

builder.writeln("Page 1.");
builder.insertBreak(aw.BreakType.PageBreak);
builder.writeln("Page 2.");
builder.insertBreak(aw.BreakType.PageBreak);
builder.writeln("Page 3.");

var stream = fs.createWriteStream(base.artifactsDir + "PdfSaveOptions.OnePage.pdf");
// Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
// to modify how that method converts the document to .PDF.
let options = new aw.Saving.PdfSaveOptions();

// Set the "PageIndex" to "1" to render a portion of the document starting from the second page.
options.pageSet = new aw.Saving.PageSet(1);

// This document will contain one page starting from page two, which will only contain the second page.
doc.save(stream, options);
await new Promise(resolve => stream.on("finish", resolve));
```

Shows how to export Odd pages from the document.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

for (let i = 0; i < 5; i++)
{
  builder.writeln(`Page ${i + 1} (${(i % 2 == 0 ? "odd" : "even")})`);
  if (i < 4)
    builder.insertBreak(aw.BreakType.PageBreak);
}

// Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
// to modify how that method converts the document to .PDF.
let options = new aw.Saving.PdfSaveOptions();

// Below are three PageSet properties that we can use to filter out a set of pages from
// our document to save in an output PDF document based on the parity of their page numbers.
// 1 -  Save only the even-numbered pages:
options.pageSet = aw.Saving.PageSet.even;

doc.save(base.artifactsDir + "PdfSaveOptions.ExportPageSet.even.pdf", options);

// 2 -  Save only the odd-numbered pages:
options.pageSet = aw.Saving.PageSet.odd;

doc.save(base.artifactsDir + "PdfSaveOptions.ExportPageSet.odd.pdf", options);

// 3 -  Save every page:
options.pageSet = aw.Saving.PageSet.all;

doc.save(base.artifactsDir + "PdfSaveOptions.ExportPageSet.all.pdf", options);
```

### See Also

* module [Aspose.Words.Saving](../../)
* class [FixedPageSaveOptions](../)

