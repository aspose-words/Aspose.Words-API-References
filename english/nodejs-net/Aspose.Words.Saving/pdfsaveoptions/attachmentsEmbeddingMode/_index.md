---
title: PdfSaveOptions.attachmentsEmbeddingMode property
linktitle: attachmentsEmbeddingMode property
articleTitle: attachmentsEmbeddingMode property
second_title: Aspose.Words for Node.js
description: "PdfSaveOptions.attachmentsEmbeddingMode property. Gets or sets a value determining how attachments are embedded to the PDF document."
type: docs
weight: 30
url: /nodejs-net/aspose.words.saving/pdfsaveoptions/attachmentsEmbeddingMode/
---

## PdfSaveOptions.attachmentsEmbeddingMode property

Gets or sets a value determining how attachments are embedded to the PDF document.


```js
get attachmentsEmbeddingMode(): Aspose.Words.Saving.PdfAttachmentsEmbeddingMode
```

### Remarks

Default value is [PdfAttachmentsEmbeddingMode.None](../../pdfattachmentsembeddingmode/#None) and attachments are not embedded.

PDF/A-1, PDF/A-2 and regular PDF/A-4 (not PDF/A-4f) standards do not allow embedded files.
[PdfAttachmentsEmbeddingMode.None](../../pdfattachmentsembeddingmode/#None) value will be used automatically.





### Examples

Shows how to add embed attachments to the PDF document.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

builder.insertOleObject(base.myDir + "Spreadsheet.xlsx", "Excel.Sheet", false, true, null);

let saveOptions = new aw.Saving.PdfSaveOptions();
saveOptions.attachmentsEmbeddingMode = aw.Saving.PdfAttachmentsEmbeddingMode.Annotations;

doc.save(base.artifactsDir + "PdfSaveOptions.PdfEmbedAttachments.pdf", saveOptions);
```

### See Also

* module [Aspose.Words.Saving](../../)
* class [PdfSaveOptions](../)

