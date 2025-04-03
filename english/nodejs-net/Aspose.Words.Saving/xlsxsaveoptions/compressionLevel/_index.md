---
title: XlsxSaveOptions.compressionLevel property
linktitle: compressionLevel property
articleTitle: compressionLevel property
second_title: Aspose.Words for NodeJs
description: "XlsxSaveOptions.compressionLevel property. Specifies the compression level used to save document"
type: docs
weight: 20
url: /nodejs-net/aspose.words.saving/xlsxsaveoptions/compressionLevel/
---

## XlsxSaveOptions.compressionLevel property

Specifies the compression level used to save document.
The default value is [CompressionLevel.Normal](../../compressionlevel/#Normal).



```js
get compressionLevel(): Aspose.Words.Saving.CompressionLevel
```

### Examples

Shows how to compress XLSX document.

```js
let doc = new aw.Document(base.myDir + "Shape with linked chart.docx");

let xlsxSaveOptions = new aw.Saving.XlsxSaveOptions();
xlsxSaveOptions.compressionLevel = aw.Saving.CompressionLevel.Maximum; 

doc.save(base.artifactsDir + "XlsxSaveOptions.CompressXlsx.xlsx", xlsxSaveOptions);
```

### See Also

* module [Aspose.Words.Saving](../../)
* class [XlsxSaveOptions](../)

