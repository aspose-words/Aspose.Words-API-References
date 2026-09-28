---
title: FileFormatUtil.extension_to_save_format method
linktitle: extension_to_save_format method
articleTitle: extension_to_save_format method
second_title: Aspose.Words for Python
description: "FileFormatUtil.extension_to_save_format method. Converts a file name extension into a [SaveFormat](../../saveformat/) value."
type: docs
weight: 40
url: /zh/python-net/aspose.words/fileformatutil/extension_to_save_format/
---

## extension_to_save_format(extension) {#str}

Converts a file name extension into a [SaveFormat](../../saveformat/) value.



```python
def extension_to_save_format(self, extension: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| extension | str | The file extension. Can be with or without a leading dot. Case-insensitive. |

### Remarks

If the extension cannot be recognized, returns [SaveFormat.UNKNOWN](../../saveformat/#UNKNOWN).




### Exceptions

| exception | condition |
| --- | --- |
| RuntimeError (Proxy error(ArgumentNullException)) | Throws if the parameter is ``None``. |

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

