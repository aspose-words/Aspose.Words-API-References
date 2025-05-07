---
title: PageSet.odd property
linktitle: odd property
articleTitle: odd property
second_title: Aspose.Words for Node.js
description: "PageSet.odd property. Gets a set with all the odd pages of the document in their original order."
type: docs
weight: 40
url: /nodejs-net/aspose.words.saving/pageset/odd/
---

## PageSet.odd property

Gets a set with all the odd pages of the document in their original order.


```js
get odd(): Aspose.Words.Saving.PageSet
```

### Remarks

Odd pages have even indices since page indices are zero-based.


### Examples

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
* class [PageSet](../)

