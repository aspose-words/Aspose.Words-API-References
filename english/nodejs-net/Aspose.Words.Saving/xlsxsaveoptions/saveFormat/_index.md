---
title: XlsxSaveOptions.saveFormat property
linktitle: saveFormat property
articleTitle: saveFormat property
second_title: Aspose.Words for Node.js
description: "XlsxSaveOptions.saveFormat property. Specifies the format in which the document will be saved if this save options object is used"
type: docs
weight: 40
url: /nodejs-net/aspose.words.saving/xlsxsaveoptions/saveFormat/
---

## XlsxSaveOptions.saveFormat property

Specifies the format in which the document will be saved if this save options object is used.
Can only be [SaveFormat.Xlsx](../../../aspose.words/saveformat/#Xlsx).



```js
get saveFormat(): Aspose.Words.SaveFormat
```

### Examples

Shows how to compress XLSX document.

```js
let doc = new aw.Document(base.myDir + "Shape with linked chart.docx");

let xlsxSaveOptions = new aw.Saving.XlsxSaveOptions();
xlsxSaveOptions.compressionLevel = aw.Saving.CompressionLevel.Maximum;
xlsxSaveOptions.saveFormat = aw.SaveFormat.Xlsx;

doc.save(base.artifactsDir + "XlsxSaveOptions.CompressXlsx.xlsx", xlsxSaveOptions);
```

### See Also

* module [Aspose.Words.Saving](../../)
* class [XlsxSaveOptions](../)

