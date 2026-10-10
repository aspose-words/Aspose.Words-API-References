---
title: FileFormatUtil.load_format_to_save_format method
linktitle: load_format_to_save_format method
articleTitle: load_format_to_save_format method
second_title: Aspose.Words for Python
description: "FileFormatUtil.load_format_to_save_format method. Converts a [LoadFormat](../../loadformat/) value to a [SaveFormat](../../saveformat/) value if possible."
type: docs
weight: 70
url: /ar/python-net/aspose.words/fileformatutil/load_format_to_save_format/
---

## load_format_to_save_format(load_format) {#loadformat}

Converts a [LoadFormat](../../loadformat/) value to a [SaveFormat](../../saveformat/) value if possible.



```python
def load_format_to_save_format(self, load_format: aspose.words.LoadFormat):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| load_format | [LoadFormat](../../loadformat/) |  |

### Exceptions

| exception | condition |
| --- | --- |
| RuntimeError (Proxy error(ArgumentException)) | Throws when cannot convert. |

### Examples

Shows how to use the FileFormatUtil methods to detect the format of a document.

```python
# حمّل وثيقة من ملف يفتقر إلى امتداد ملف، ثم اكتشف تنسيق الملف الخاص به.
with system_helper.io.File.open_read(MY_DIR + 'Word document with missing file extension') as doc_stream:
    info = aw.FileFormatUtil.detect_file_format(stream=doc_stream)
    load_format = info.load_format
    self.assertEqual(aw.LoadFormat.DOC, load_format)
    # فيما يلي طريقتان لتحويل LoadFormat إلى SaveFormat المقابل.
    # 1 -  احصل على سلسلة امتداد الملف لـ LoadFormat، ثم احصل على SaveFormat المقابل من تلك السلسلة:
    file_extension = aw.FileFormatUtil.load_format_to_extension(load_format)
    save_format = aw.FileFormatUtil.extension_to_save_format(file_extension)
    # 2 -  حوّل LoadFormat مباشرةً إلى SaveFormat الخاص به:
    save_format = aw.FileFormatUtil.load_format_to_save_format(load_format)
    # حمّل مستندًا من الدفق، ثم احفظه بامتداد الملف المكتشف تلقائيًا.
    doc = aw.Document(stream=doc_stream)
    self.assertEqual('.doc', aw.FileFormatUtil.save_format_to_extension(save_format))
    doc.save(file_name=ARTIFACTS_DIR + 'File.SaveToDetectedFileFormat' + aw.FileFormatUtil.save_format_to_extension(save_format))
```

### See Also

* module [aspose.words](../../)
* class [FileFormatUtil](../)

