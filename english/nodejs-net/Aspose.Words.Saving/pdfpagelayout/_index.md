---
title: PdfPageLayout enumeration
linktitle: PdfPageLayout enumeration
articleTitle: PdfPageLayout enumeration
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.Saving.PdfPageLayout enumeration. Specifies the page layout to be used when the document is opened in a PDF reader."
type: docs
weight: 690
url: /nodejs-net/aspose.words.saving/pdfpagelayout/
---

## PdfPageLayout enumeration

Specifies the page layout to be used when the document is opened in a PDF reader.


### Members

| Name | Description |
| --- | --- |
| SinglePage | Display one page at a time. |
| OneColumn | Display the pages in one column. |
| TwoColumnLeft | Display the pages in two columns, with odd-numbered pages on the left. |
| TwoColumnRight | Display the pages in two columns, with odd-numbered pages on the right. |
| TwoPageLeft | Display the pages two at a time, with odd-numbered pages on the left. |
| TwoPageRight | Display the pages two at a time, with odd-numbered pages on the right. |

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

* module [Aspose.Words.Saving](../)

