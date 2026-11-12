---
title: FileFormatUtil.content_type_to_save_format method
linktitle: content_type_to_save_format method
articleTitle: content_type_to_save_format method
second_title: Aspose.Words for Python
description: "FileFormatUtil.content_type_to_save_format method. Converts IANA content type into a save format enumerated value."
type: docs
weight: 20
url: /ru/python-net/aspose.words/fileformatutil/content_type_to_save_format/
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
# Методы ContentTypeToSaveFormat/ContentTypeToLoadFormat принимают только официальные названия медиа‑типов IANA, также известные как MIME‑типы.
# Все действительные медиа‑типы перечислены здесь: https:#www.iana.org/assignments/media-types/media-types.xhtml.
# Попытка связать SaveFormat с частичной строкой медиа‑типа не сработает.
self.assertRaises(Exception, lambda: aw.FileFormatUtil.content_type_to_save_format('jpeg'))
# Если у Aspose.Words нет соответствующего формата сохранения/загрузки для типа контента, также будет выброшено исключение.
self.assertRaises(Exception, lambda: aw.FileFormatUtil.content_type_to_save_format('application/zip'))
# Файлы перечисленных ниже типов можно сохранять, но не загружать с помощью Aspose.Words.
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
# Для типов файлов, которые можно сохранять и загружать, мы можем сопоставить медиа‑тип как формату загрузки, так и формату сохранения.
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

