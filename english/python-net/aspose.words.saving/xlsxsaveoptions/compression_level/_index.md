---
title: XlsxSaveOptions.compression_level property
linktitle: compression_level property
articleTitle: compression_level property
second_title: Aspose.Words for Python
description: "XlsxSaveOptions.compression_level property. Specifies the compression level used to save document"
type: docs
weight: 20
url: /python-net/aspose.words.saving/xlsxsaveoptions/compression_level/
---

## XlsxSaveOptions.compression_level property

Specifies the compression level used to save document.
The default value is [CompressionLevel.NORMAL](../../compressionlevel/#NORMAL).



### Examples

Shows how to compress XLSX document.

```python
doc = Document(MY_DIR + "Shape with linked chart.docx")

xlsx_save_options = XlsxSaveOptions()
xlsx_save_options.compression_level = CompressionLevel.MAXIMUM

doc.save(ARTIFACTS_DIR + "XlsxSaveOptions.CompressXlsx.xlsx", xlsx_save_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [XlsxSaveOptions](../)

