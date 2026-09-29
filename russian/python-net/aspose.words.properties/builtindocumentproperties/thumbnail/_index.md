---
title: BuiltInDocumentProperties.thumbnail property
linktitle: thumbnail property
articleTitle: thumbnail property
second_title: Aspose.Words for Python
description: "BuiltInDocumentProperties.thumbnail property. Gets or sets the thumbnail of the document."
type: docs
weight: 310
url: /ru/python-net/aspose.words.properties/builtindocumentproperties/thumbnail/
---

## BuiltInDocumentProperties.thumbnail property

Gets or sets the thumbnail of the document.




```python
@property
def thumbnail(self) -> bytes:
    ...

@thumbnail.setter
def thumbnail(self, value: bytes):
    ...

```

### Exceptions

| exception | condition |
| --- | --- |
| RuntimeError (Proxy error(InvalidOperationException)) | Thrown if the image is invalid or its format is unsupported for specific format of document. |

### Remarks

For now this property is used only when a document is being exported to ePub,
it's not read from and written to other document formats.

Image of arbitrary format can be set to this property, but the format is checked during export.

Only gif, jpeg and png images can be used for ePub publication.




### Examples

Shows how to add a thumbnail to a document that we save as an Epub.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('Hello world!')
# Если мы сохраняем документ, у которого свойство "Thumbnail" содержит добавленные нами данные изображения, в формате Epub,
# чтение, открывающее этот документ, может отобразить изображение перед первой страницей.
properties = doc.built_in_document_properties
thumbnail_bytes = system_helper.io.File.read_all_bytes(IMAGE_DIR + 'Logo.jpg')
properties.thumbnail = thumbnail_bytes
doc.save(file_name=ARTIFACTS_DIR + 'DocumentProperties.Thumbnail.epub')
# Мы можем извлечь изображение миниатюры документа и сохранить его в локальную файловую систему.
thumbnail = doc.built_in_document_properties.get_by_name('Thumbnail')
system_helper.io.File.write_all_bytes(ARTIFACTS_DIR + 'DocumentProperties.Thumbnail.gif', thumbnail.to_byte_array())
```

### See Also

* module [aspose.words.properties](../../)
* class [BuiltInDocumentProperties](../)

