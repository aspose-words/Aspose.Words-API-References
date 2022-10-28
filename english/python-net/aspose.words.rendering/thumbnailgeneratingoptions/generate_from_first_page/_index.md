---
title: generate_from_first_page property
second_title: Aspose.Words for Python via .NET API Reference
description: "Specifies whether to generate thumbnail from first page of the document or first image."
type: docs
weight: 20
url: /python-net/aspose.words.rendering/thumbnailgeneratingoptions/generate_from_first_page/
---

## ThumbnailGeneratingOptions.generate_from_first_page property

Specifies whether to generate thumbnail from first page of the document or first image.

Default is ``True``, which means thumbnail will be generated from first page of the document.
If value is ``False`` and there is no image in the document, thumbnail will be generated 
from first page of the document.



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
self.assertEqual(drawing.Size(600, 900), options.thumbnail_size) #ExSKip
options.thumbnail_size = drawing.Size(400, 400)
options.generate_from_first_page = False

doc.update_thumbnail(options)
doc.save(ARTIFACTS_DIR + "Document.update_thumbnail.first_image.epub")
```

### See Also

* module [aspose.words.rendering](../../)
* class [ThumbnailGeneratingOptions](../)

