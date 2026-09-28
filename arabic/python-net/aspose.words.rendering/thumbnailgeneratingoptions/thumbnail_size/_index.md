---
title: ThumbnailGeneratingOptions.thumbnail_size property
linktitle: thumbnail_size property
articleTitle: thumbnail_size property
second_title: Aspose.Words for Python
description: "ThumbnailGeneratingOptions.thumbnail_size property. Size of generated thumbnail in pixels"
type: docs
weight: 30
url: /ar/python-net/aspose.words.rendering/thumbnailgeneratingoptions/thumbnail_size/
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
# هناك طريقتان لتعيين صورة مصغرة عند حفظ مستند إلى .epub.
# 1 -  استخدم الصفحة الأولى للمستند:
doc.update_thumbnail()
doc.save(file_name=ARTIFACTS_DIR + 'Document.UpdateThumbnail.FirstPage.epub')
# 2 -  استخدم الصورة الأولى الموجودة في المستند:
options = aw.rendering.ThumbnailGeneratingOptions()
options.thumbnail_size = aspose.pydrawing.Size(400, 400)
options.generate_from_first_page = False
doc.update_thumbnail(options)
doc.save(file_name=ARTIFACTS_DIR + 'Document.UpdateThumbnail.FirstImage.epub')
```

### See Also

* module [aspose.words.rendering](../../)
* class [ThumbnailGeneratingOptions](../)

