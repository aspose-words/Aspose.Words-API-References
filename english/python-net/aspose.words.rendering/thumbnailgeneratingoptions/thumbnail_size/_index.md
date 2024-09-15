---
title: ThumbnailGeneratingOptions.thumbnail_size property
linktitle: thumbnail_size property
articleTitle: thumbnail_size property
second_title: Aspose.Words for Python
description: "ThumbnailGeneratingOptions.thumbnail_size property. Size of generated thumbnail in pixels"
type: docs
weight: 30
url: /python-net/aspose.words.rendering/thumbnailgeneratingoptions/thumbnail_size/
---

## ThumbnailGeneratingOptions.thumbnail_size property

Size of generated thumbnail in pixels.
Default is 600x900.


```python
@property
def thumbnail_size(self) -> aspose.pydrawing.Size:
    ...

@thumbnail_size.setter
def thumbnail_size(self, value: aspose.pydrawing.Size):
    ...

```

### Examples

Shows how to update a document's thumbnail.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('Hello world!')
builder.insert_image(file_name=IMAGE_DIR + 'Logo.jpg')
# There are two ways of setting a thumbnail image when saving a document to .epub.
# 1 -  Use the document's first page:
doc.update_thumbnail()
doc.save(file_name=ARTIFACTS_DIR + 'Document.UpdateThumbnail.FirstPage.epub')
# 2 -  Use the first image found in the document:
options = aw.rendering.ThumbnailGeneratingOptions()
options.thumbnail_size = aspose.pydrawing.Size(400, 400)
options.generate_from_first_page = False
doc.update_thumbnail(options)
doc.save(file_name=ARTIFACTS_DIR + 'Document.UpdateThumbnail.FirstImage.epub')
```

### See Also

* module [aspose.words.rendering](../../)
* class [ThumbnailGeneratingOptions](../)

