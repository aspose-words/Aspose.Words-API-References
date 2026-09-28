---
title: RtfSaveOptions.save_format property
linktitle: save_format property
articleTitle: save_format property
second_title: Aspose.Words for Python
description: "RtfSaveOptions.save_format property. Specifies the format in which the document will be saved if this save options object is used"
type: docs
weight: 40
url: /zh/python-net/aspose.words.saving/rtfsaveoptions/save_format/
---

## RtfSaveOptions.save_format property

Specifies the format in which the document will be saved if this save options object is used.
Can only be [SaveFormat.RTF](../../../aspose.words/saveformat/#RTF).



```python
@property
def save_format(self) -> aspose.words.SaveFormat:
    ...

@save_format.setter
def save_format(self, value: aspose.words.SaveFormat):
    ...

```

### Examples

Shows how to save a document to .rtf with custom options.

```python
doc = aw.Document(file_name=MY_DIR + 'Rendering.docx')
# 创建一个 "RtfSaveOptions" 对象，以传递给文档的 "Save" 方法，修改我们将其保存为 RTF 的方式。
options = aw.saving.RtfSaveOptions()
self.assertEqual(aw.SaveFormat.RTF, options.save_format)
# 将 "ExportCompactSize" 属性设置为 "true"，以
# 在牺牲从右到左文本兼容性的情况下减小已保存文档的大小。
options.export_compact_size = True
# 将 "ExportImagesFotOldReaders" 属性设置为 "true"，以使用额外的关键字来确保我们的文档
# 兼容 Microsoft Word 97 之前的阅读器和 WordPad。
# 将 "ExportImagesFotOldReaders" 属性设置为 "false"，以减小文档的大小，
# 但会阻止旧阅读器读取文档可能包含的任何非元文件或 BMP 图像。
options.export_images_for_old_readers = export_images_for_old_readers
doc.save(file_name=ARTIFACTS_DIR + 'RtfSaveOptions.ExportImages.rtf', save_options=options)
```

### See Also

* module [aspose.words.saving](../../)
* class [RtfSaveOptions](../)

