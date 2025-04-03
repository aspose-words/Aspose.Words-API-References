---
title: PdfSaveOptions.pageLayout property
linktitle: pageLayout property
articleTitle: pageLayout property
second_title: Aspose.Words for NodeJs
description: "PdfSaveOptions.pageLayout property. Specifies the page layout to be used when the document is opened in a PDF reader."
type: docs
weight: 250
url: /nodejs-net/aspose.words.saving/pdfsaveoptions/pageLayout/
---

## PdfSaveOptions.pageLayout property

Specifies the page layout to be used when the document is opened in a PDF reader.


```js
get pageLayout(): Aspose.Words.Saving.PdfPageLayout
```

### Remarks

The default value is [PdfPageLayout.SinglePage](../../pdfpagelayout/#SinglePage).



### Examples

Shows how to display pages when opened in a PDF reader.

```js
let doc = new aw.Document(base.myDir + "Big document.docx");

// Display the pages two at a time, with odd-numbered pages on the left.
let saveOptions = new aw.Saving.PdfSaveOptions();
saveOptions.pageLayout = aw.Saving.PdfPageLayout.TwoPageLeft;

doc.save(base.artifactsDir + "PdfSaveOptions.pageLayout.pdf", saveOptions);
```

### See Also

* module [Aspose.Words.Saving](../../)
* class [PdfSaveOptions](../)

