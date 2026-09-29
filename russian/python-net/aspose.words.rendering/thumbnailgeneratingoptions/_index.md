---
title: ThumbnailGeneratingOptions class
linktitle: ThumbnailGeneratingOptions class
articleTitle: ThumbnailGeneratingOptions class
second_title: Aspose.Words for Python
description: "aspose.words.rendering.ThumbnailGeneratingOptions class. Can be used to specify additional options when generating thumbnail for a document."
type: docs
weight: 50
url: /ru/python-net/aspose.words.rendering/thumbnailgeneratingoptions/
---

## ThumbnailGeneratingOptions class

Can be used to specify additional options when generating thumbnail for a document.


### Remarks

User can call method [Document.update_thumbnail()](../../aspose.words/document/update_thumbnail/#thumbnailgeneratingoptions) to generate 
[BuiltInDocumentProperties.thumbnail](../../aspose.words.properties/builtindocumentproperties/thumbnail/) for a document.



### Constructors
| Name | Description |
| --- | --- |
| [ThumbnailGeneratingOptions()](./__init__/#default) | The default constructor. |

### Properties

| Name | Description |
| --- | --- |
| [generate_from_first_page](./generate_from_first_page/) | Specifies whether to generate thumbnail from first page of the document or first image. |
| [thumbnail_size](./thumbnail_size/) | Size of generated thumbnail in pixels. Default is 600x900. |

### Examples

Shows how to update a document's thumbnail.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('Hello world!')
builder.insert_image(file_name=IMAGE_DIR + 'Logo.jpg')
# Существует два способа установить изображение миниатюры при сохранении документа в .epub.
# 1 -  Использовать первую страницу документа:
doc.update_thumbnail()
doc.save(file_name=ARTIFACTS_DIR + 'Document.UpdateThumbnail.FirstPage.epub')
# 2 -  Использовать первое найденное в документе изображение:
options = aw.rendering.ThumbnailGeneratingOptions()
options.thumbnail_size = aspose.pydrawing.Size(400, 400)
options.generate_from_first_page = False
doc.update_thumbnail(options)
doc.save(file_name=ARTIFACTS_DIR + 'Document.UpdateThumbnail.FirstImage.epub')
```

### See Also

* module [aspose.words.rendering](../)

