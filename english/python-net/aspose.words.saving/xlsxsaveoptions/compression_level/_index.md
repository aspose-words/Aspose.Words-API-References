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



```python
@property
def compression_level(self) -> aspose.words.saving.CompressionLevel:
    ...

@compression_level.setter
def compression_level(self, value: aspose.words.saving.CompressionLevel):
    ...

```

### Examples

Shows how to compress XLSX document.

```python
doc = aw.Document(file_name=MY_DIR + 'Shape with linked chart.docx')
xlsx_save_options = aw.saving.XlsxSaveOptions()
xlsx_save_options.compression_level = aw.saving.CompressionLevel.MAXIMUM
xlsx_save_options.save_format = aw.SaveFormat.XLSX
doc.save(file_name=ARTIFACTS_DIR + 'XlsxSaveOptions.CompressXlsx.xlsx', save_options=xlsx_save_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [XlsxSaveOptions](../)

