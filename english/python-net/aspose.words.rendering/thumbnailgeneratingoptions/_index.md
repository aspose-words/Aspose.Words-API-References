---
title: ThumbnailGeneratingOptions class
linktitle: ThumbnailGeneratingOptions class
articleTitle: ThumbnailGeneratingOptions class
second_title: Aspose.Words for Python
description: "aspose.words.rendering.ThumbnailGeneratingOptions class. Can be used to specify additional options when generating thumbnail for a document."
type: docs
weight: 50
url: /python-net/aspose.words.rendering/thumbnailgeneratingoptions/
---

## ThumbnailGeneratingOptions class

Can be used to specify additional options when generating thumbnail for a document.


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
builder = aw.DocumentBuilder(doc)

builder.writeln("Hello world!")
builder.insert_image(IMAGE_DIR + "Logo.jpg")

# There are two ways of setting a thumbnail image when saving a document to .epub.
# 1 -  Use the document's first page:
doc.update_thumbnail()
doc.save(ARTIFACTS_DIR + "Document.update_thumbnail.first_page.epub")

# 2 -  Use the first image found in the document:
options = aw.rendering.ThumbnailGeneratingOptions()
options.thumbnail_size = drawing.Size(400, 400)
options.generate_from_first_page = False

doc.update_thumbnail(options)
doc.save(ARTIFACTS_DIR + "Document.update_thumbnail.first_image.epub")
```

### See Also

* module [aspose.words.rendering](../)

