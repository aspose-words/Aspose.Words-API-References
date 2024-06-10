---
title: FileFormatUtil.content_type_to_save_format method
linktitle: content_type_to_save_format method
articleTitle: content_type_to_save_format method
second_title: Aspose.Words for Python
description: "FileFormatUtil.content_type_to_save_format method. Converts IANA content type into a save format enumerated value."
type: docs
weight: 20
url: /python-net/aspose.words/fileformatutil/content_type_to_save_format/
---

## content_type_to_save_format(content_type) {#str}

Converts IANA content type into a save format enumerated value.


```python
def content_type_to_save_format(self, content_type: str):
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
# The content_type_to_save_format/content_type_to_load_format methods only accept official IANA media type names, also known as MIME types.
# All valid media types are listed here: https://www.iana.org/assignments/media-types/media-types.xhtml.
# Trying to associate a SaveFormat with a partial media type string will not work.
with self.assertRaises(Exception):
    aw.FileFormatUtil.content_type_to_save_format('jpeg')
# If Aspose.Words does not have a corresponding save/load format for a content type, an exception will also be thrown.
with self.assertRaises(Exception):
    aw.FileFormatUtil.content_type_to_save_format('application/zip')
# Files of the types listed below can be saved, but not loaded using Aspose.Words.
with self.assertRaises(Exception):
    aw.FileFormatUtil.content_type_to_load_format('image/jpeg')
self.assertEqual(aw.SaveFormat.JPEG, aw.FileFormatUtil.content_type_to_save_format('image/jpeg'))
self.assertEqual(aw.SaveFormat.PNG, aw.FileFormatUtil.content_type_to_save_format('image/png'))
self.assertEqual(aw.SaveFormat.TIFF, aw.FileFormatUtil.content_type_to_save_format('image/tiff'))
self.assertEqual(aw.SaveFormat.GIF, aw.FileFormatUtil.content_type_to_save_format('image/gif'))
self.assertEqual(aw.SaveFormat.EMF, aw.FileFormatUtil.content_type_to_save_format('image/x-emf'))
self.assertEqual(aw.SaveFormat.XPS, aw.FileFormatUtil.content_type_to_save_format('application/vnd.ms-xpsdocument'))
self.assertEqual(aw.SaveFormat.PDF, aw.FileFormatUtil.content_type_to_save_format('application/pdf'))
self.assertEqual(aw.SaveFormat.SVG, aw.FileFormatUtil.content_type_to_save_format('image/svg+xml'))
self.assertEqual(aw.SaveFormat.EPUB, aw.FileFormatUtil.content_type_to_save_format('application/epub+zip'))
# For file types that can be saved and loaded, we can match a media type to both a load format and a save format.
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

