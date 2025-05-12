---
title: PdfLoadOptions.pageCount property
linktitle: pageCount property
articleTitle: pageCount property
second_title: Aspose.Words for Node.js
description: "PdfLoadOptions.pageCount property. Gets or sets the number of pages to read"
type: docs
weight: 20
url: /nodejs-net/aspose.words.loading/pdfloadoptions/pageCount/
---

## PdfLoadOptions.pageCount property

Gets or sets the number of pages to read. Default is MaxValue which means all pages of the document will be read.


```js
get pageCount(): number
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

