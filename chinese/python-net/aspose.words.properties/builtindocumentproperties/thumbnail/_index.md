---
title: BuiltInDocumentProperties.thumbnail property
linktitle: thumbnail property
articleTitle: thumbnail property
second_title: Aspose.Words for Python
description: "BuiltInDocumentProperties.thumbnail property. Gets or sets the thumbnail of the document."
type: docs
weight: 310
url: /zh/python-net/aspose.words.properties/builtindocumentproperties/thumbnail/
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
# 如果我们将一个文档（其 "Thumbnail" 属性包含我们添加的图像数据）保存为 Epub，
# 打开该文档的阅读器可能会在第一页之前显示该图像。
properties = doc.built_in_document_properties
thumbnail_bytes = system_helper.io.File.read_all_bytes(IMAGE_DIR + 'Logo.jpg')
properties.thumbnail = thumbnail_bytes
doc.save(file_name=ARTIFACTS_DIR + 'DocumentProperties.Thumbnail.epub')
# 我们可以提取文档的缩略图并将其保存到本地文件系统。
thumbnail = doc.built_in_document_properties.get_by_name('Thumbnail')
system_helper.io.File.write_all_bytes(ARTIFACTS_DIR + 'DocumentProperties.Thumbnail.gif', thumbnail.to_byte_array())
```

### See Also

* module [aspose.words.properties](../../)
* class [BuiltInDocumentProperties](../)

