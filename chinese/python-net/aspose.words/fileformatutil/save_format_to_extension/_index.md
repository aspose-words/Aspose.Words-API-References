---
title: FileFormatUtil.save_format_to_extension method
linktitle: save_format_to_extension method
articleTitle: save_format_to_extension method
second_title: Aspose.Words for Python
description: "FileFormatUtil.save_format_to_extension method. Converts a save format enumerated value into a file extension"
type: docs
weight: 80
url: /zh/python-net/aspose.words/fileformatutil/save_format_to_extension/
---

## save_format_to_extension(save_format) {#saveformat}

Converts a save format enumerated value into a file extension. The returned extension is a lower-case string with a leading dot.


```python
def save_format_to_extension(self, save_format: aspose.words.SaveFormat):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| save_format | [SaveFormat](../../saveformat/) |  |

### Remarks

The [SaveFormat.WORD_ML](../../saveformat/#WORD_ML) value is converted to ".wml".

The [SaveFormat.FLAT_OPC](../../saveformat/#FLAT_OPC) value is converted to ".fopc".




### Exceptions

| exception | condition |
| --- | --- |
| RuntimeError (Proxy error(ArgumentException)) | Throws when cannot convert. |

### Examples

Shows how to use the FileFormatUtil methods to detect the format of a document.

```python
# 从缺少文件扩展名的文件加载文档，然后检测其文件格式。
with system_helper.io.File.open_read(MY_DIR + 'Word document with missing file extension') as doc_stream:
    info = aw.FileFormatUtil.detect_file_format(stream=doc_stream)
    load_format = info.load_format
    self.assertEqual(aw.LoadFormat.DOC, load_format)
    # 下面是两种将 LoadFormat 转换为相应 SaveFormat 的方法。
    # 1 - 获取 LoadFormat 的文件扩展名字符串，然后从该字符串获取相应的 SaveFormat：
    file_extension = aw.FileFormatUtil.load_format_to_extension(load_format)
    save_format = aw.FileFormatUtil.extension_to_save_format(file_extension)
    # 2 - 将 LoadFormat 直接转换为其 SaveFormat：
    save_format = aw.FileFormatUtil.load_format_to_save_format(load_format)
    # 从流中加载文档，然后将其保存为自动检测的文件扩展名。
    doc = aw.Document(stream=doc_stream)
    self.assertEqual('.doc', aw.FileFormatUtil.save_format_to_extension(save_format))
    doc.save(file_name=ARTIFACTS_DIR + 'File.SaveToDetectedFileFormat' + aw.FileFormatUtil.save_format_to_extension(save_format))
```

### See Also

* module [aspose.words](../../)
* class [FileFormatUtil](../)

