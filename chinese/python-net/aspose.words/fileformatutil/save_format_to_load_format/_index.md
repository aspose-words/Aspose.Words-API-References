---
title: FileFormatUtil.save_format_to_load_format method
linktitle: save_format_to_load_format method
articleTitle: save_format_to_load_format method
second_title: Aspose.Words for Python
description: "FileFormatUtil.save_format_to_load_format method. Converts a [SaveFormat](../../saveformat/) value to a [LoadFormat](../../loadformat/) value if possible."
type: docs
weight: 90
url: /zh/python-net/aspose.words/fileformatutil/save_format_to_load_format/
---

## save_format_to_load_format(save_format) {#saveformat}

Converts a [SaveFormat](../../saveformat/) value to a [LoadFormat](../../loadformat/) value if possible.



```python
def save_format_to_load_format(self, save_format: aspose.words.SaveFormat):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| save_format | [SaveFormat](../../saveformat/) |  |

### Exceptions

| exception | condition |
| --- | --- |
| RuntimeError (Proxy error(ArgumentException)) | Throws when cannot convert. |

### Examples

Shows how to convert a save format to its corresponding load format.

```python
self.assertEqual(aw.LoadFormat.HTML, aw.FileFormatUtil.save_format_to_load_format(aw.SaveFormat.HTML))
# 某些文件类型可以使用 Aspose.Words 将文档保存，但不能加载。
# 如果我们尝试将此类的保存格式转换为加载格式，将抛出异常。
self.assertRaises(Exception, lambda: aw.FileFormatUtil.save_format_to_load_format(aw.SaveFormat.JPEG))
```

### See Also

* module [aspose.words](../../)
* class [FileFormatUtil](../)

