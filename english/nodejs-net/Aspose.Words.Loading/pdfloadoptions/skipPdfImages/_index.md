---
title: PdfLoadOptions.skipPdfImages property
linktitle: skipPdfImages property
articleTitle: skipPdfImages property
second_title: Aspose.Words for Node.js
description: "PdfLoadOptions.skipPdfImages property. Gets or sets the flag indicating whether images must be skipped while loading PDF document"
type: docs
weight: 40
url: /nodejs-net/aspose.words.loading/pdfloadoptions/skipPdfImages/
---

## PdfLoadOptions.skipPdfImages property

Gets or sets the flag indicating whether images must be skipped while loading PDF document. Default is ``false``.



```js
get skipPdfImages(): boolean
```

### Examples

Shows how to skip images during loading PDF files.

```js
let options = new aw.Loading.PdfLoadOptions();
options.skipPdfImages = isSkipPdfImages;
options.pageIndex = 0;
options.pageCount = 1;

let doc = new aw.Document(base.myDir + "Images.pdf", options);
let shapeCollection = doc.getChildNodes(aw.NodeType.Shape, true);

if (isSkipPdfImages)
  expect(shapeCollection.count).toEqual(0);
else
  expect(shapeCollection.count).not.toEqual(0);
```

### See Also

* module [Aspose.Words.Loading](../../)
* class [PdfLoadOptions](../)

