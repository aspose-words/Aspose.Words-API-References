---
title: PdfLoadOptions.pageIndex property
linktitle: pageIndex property
articleTitle: pageIndex property
second_title: Aspose.Words for Node.js
description: "PdfLoadOptions.pageIndex property. Gets or sets the 0-based index of the first page to read"
type: docs
weight: 30
url: /nodejs-net/aspose.words.loading/pdfloadoptions/pageIndex/
---

## PdfLoadOptions.pageIndex property

Gets or sets the 0-based index of the first page to read. Default is 0.


```js
get pageIndex(): number
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

