---
title: FileFormatUtil.content_type_to_load_format method
linktitle: content_type_to_load_format method
articleTitle: content_type_to_load_format method
second_title: Aspose.Words for Python
description: "FileFormatUtil.content_type_to_load_format method. Converts IANA content type into a load format enumerated value."
type: docs
weight: 10
url: /zh/python-net/aspose.words/fileformatutil/content_type_to_load_format/
---

## content_type_to_load_format(content_type) {#str}

Converts IANA content type into a load format enumerated value.


```python
def content_type_to_load_format(self, content_type: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| content_type | str |  |

### Exceptions

| exception | condition |
| --- | --- |
| RuntimeError (Proxy error(ArgumentException)) | Throws when cannot convert. |

### Examples

Shows how to find the corresponding Aspose load/save format from each media type string.

```python
# ContentTypeToSaveFormat/ContentTypeToLoadFormat 方法仅接受官方 IANA 媒体类型名称，也称为 MIME 类型。
# 所有有效的媒体类型列在此处：https:#www.iana.org/assignments/media-types/media-types.xhtml。
# 尝试将 SaveFormat 与部分媒体类型字符串关联将不起作用。
self.assertRaises(Exception, lambda: aw.FileFormatUtil.content_type_to_save_format('jpeg'))
# 如果 Aspose.Words 没有对应的内容类型的保存/加载格式，也会抛出异常。
self.assertRaises(Exception, lambda: aw.FileFormatUtil.content_type_to_save_format('application/zip'))
# 下面列出的类型的文件可以使用 Aspose.Words 保存，但不能加载。
self.assertRaises(Exception, lambda: aw.FileFormatUtil.content_type_to_load_format('image/jpeg'))
self.assertEqual(aw.SaveFormat.JPEG, aw.FileFormatUtil.content_type_to_save_format('image/jpeg'))
self.assertEqual(aw.SaveFormat.PNG, aw.FileFormatUtil.content_type_to_save_format('image/png'))
self.assertEqual(aw.SaveFormat.TIFF, aw.FileFormatUtil.content_type_to_save_format('image/tiff'))
self.assertEqual(aw.SaveFormat.GIF, aw.FileFormatUtil.content_type_to_save_format('image/gif'))
self.assertEqual(aw.SaveFormat.EMF, aw.FileFormatUtil.content_type_to_save_format('image/x-emf'))
self.assertEqual(aw.SaveFormat.XPS, aw.FileFormatUtil.content_type_to_save_format('application/vnd.ms-xpsdocument'))
self.assertEqual(aw.SaveFormat.PDF, aw.FileFormatUtil.content_type_to_save_format('application/pdf'))
self.assertEqual(aw.SaveFormat.SVG, aw.FileFormatUtil.content_type_to_save_format('image/svg+xml'))
self.assertEqual(aw.SaveFormat.EPUB, aw.FileFormatUtil.content_type_to_save_format('application/epub+zip'))
# 对于既可保存又可加载的文件类型，我们可以将媒体类型匹配到加载格式和保存格式。
self.assertEqual(aw.LoadFormat.DOC, aw.FileFormatUtil.content_type_to_load_format('application/msword'))
self.assertEqual(aw.SaveFormat.DOC, aw.FileFormatUtil.content_type_to_save_format('application/msword'))
self.assertEqual(aw.LoadFormat.DOCX, aw.FileFormatUtil.content_type_to_load_format('application/vnd.openxmlformats-officedocument.wordprocessingml.document'))
self.assertEqual(aw.SaveFormat.DOCX, aw.FileFormatUtil.content_type_to_save_format('application/vnd.openxmlformats-officedocument.wordprocessingml.document'))
self.assertEqual(aw.LoadFormat.TEXT, aw.FileFormatUtil.content_type_to_load_format('text/plain'))
self.assertEqual(aw.SaveFormat.TEXT, aw.FileFormatUtil.content_type_to_save_format('text/plain'))
self.assertEqual(aw.LoadFormat.RTF, aw.FileFormatUtil.content_type_to_load_format('application/rtf'))
self.assertEqual(aw.SaveFormat.RTF, aw.FileFormatUtil.content_type_to_save_format('application/rtf'))
self.assertEqual(aw.LoadFormat.HTML, aw.FileFormatUtil.content_type_to_load_format('text/html'))
self.assertEqual(aw.SaveFormat.HTML, aw.FileFormatUtil.content_type_to_save_format('text/html'))
self.assertEqual(aw.LoadFormat.MHTML, aw.FileFormatUtil.content_type_to_load_format('multipart/related'))
self.assertEqual(aw.SaveFormat.MHTML, aw.FileFormatUtil.content_type_to_save_format('multipart/related'))
```

### See Also

* module [aspose.words](../../)
* class [FileFormatUtil](../)

