---
title: ThumbnailGeneratingOptions.generate_from_first_page property
linktitle: generate_from_first_page property
articleTitle: generate_from_first_page property
second_title: Aspose.Words for Python
description: "ThumbnailGeneratingOptions.generate_from_first_page property. Specifies whether to generate thumbnail from first page of the document or first image."
type: docs
weight: 20
url: /ar/python-net/aspose.words.rendering/thumbnailgeneratingoptions/generate_from_first_page/
---

## ThumbnailGeneratingOptions.generate_from_first_page property

Specifies whether to generate thumbnail from first page of the document or first image.


```python
@property
def generate_from_first_page(self) -> bool:
    ...

@generate_from_first_page.setter
def generate_from_first_page(self, value: bool):
    ...

```

### Remarks

Default is ``True``, which means thumbnail will be generated from first page of the document.
If value is ``False`` and there is no image in the document, thumbnail will be generated 
from first page of the document.



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

