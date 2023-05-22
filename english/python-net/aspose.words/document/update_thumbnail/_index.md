---
title: Document.update_thumbnail method
linktitle: update_thumbnail method
articleTitle: update_thumbnail method
second_title: Aspose.Words for Python
description: "aspose.words.Document.update_thumbnail method"
type: docs
weight: 760
url: /python-net/aspose.words/document/update_thumbnail/
---

## update_thumbnail(options) {#thumbnailgeneratingoptions}

Updates [BuiltInDocumentProperties.thumbnail](../../../aspose.words.properties/builtindocumentproperties/thumbnail/) of the document according to the specified options.



```python
def update_thumbnail(self, options: aspose.words.rendering.ThumbnailGeneratingOptions):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| options | [ThumbnailGeneratingOptions](../../../aspose.words.rendering/thumbnailgeneratingoptions/) |  |

The [ThumbnailGeneratingOptions](../../../aspose.words.rendering/thumbnailgeneratingoptions/) allows you to specify the source of thumbnail, size and other options.
If attempt to generate thumbnail fails, doesn't change one.



## update_thumbnail() {#default}

Updates [BuiltInDocumentProperties.thumbnail](../../../aspose.words.properties/builtindocumentproperties/thumbnail/) of the document using default options.



```python
def update_thumbnail(self):
    ...
```

## Examples

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

## See Also

* module [aspose.words](../../)
* class [Document](../)

