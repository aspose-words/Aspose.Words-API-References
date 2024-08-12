---
title: XlsxSaveOptions.save_format property
linktitle: save_format property
articleTitle: save_format property
second_title: Aspose.Words for Python
description: "XlsxSaveOptions.save_format property. Specifies the format in which the document will be saved if this save options object is used"
type: docs
weight: 40
url: /python-net/aspose.words.saving/xlsxsaveoptions/save_format/
---

## XlsxSaveOptions.save_format property

Specifies the format in which the document will be saved if this save options object is used.
Can only be [SaveFormat.XLSX](../../../aspose.words/saveformat/#XLSX).



```python
@property
def save_format(self) -> aspose.words.SaveFormat:
    ...

@save_format.setter
def save_format(self, value: aspose.words.SaveFormat):
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

