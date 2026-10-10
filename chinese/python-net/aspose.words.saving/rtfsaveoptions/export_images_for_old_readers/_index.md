---
title: RtfSaveOptions.export_images_for_old_readers property
linktitle: export_images_for_old_readers property
articleTitle: export_images_for_old_readers property
second_title: Aspose.Words for Python
description: "RtfSaveOptions.export_images_for_old_readers property. Specifies whether the keywords for old readers are written to RTF or not"
type: docs
weight: 30
url: /zh/python-net/aspose.words.saving/rtfsaveoptions/export_images_for_old_readers/
---

## RtfSaveOptions.export_images_for_old_readers property

Specifies whether the keywords for "old readers" are written to RTF or not.
This can significantly affect the size of the RTF document.

Default value is ``True``.



```python
@property
def export_images_for_old_readers(self) -> bool:
    ...

@export_images_for_old_readers.setter
def export_images_for_old_readers(self, value: bool):
    ...

```

### Remarks

"Old readers" are pre-Microsoft Word 97 applications and also WordPad.
When this option is ``True`` Aspose.Words writes additional RTF keywords.
These keywords allow the document to be displayed correctly when opened in an 
"old reader" application, but can significantly increase the size of the document.

If you set this option to ``False``, then only images in WMF, EMF and BMP formats
will be displayed in "old readers".




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

