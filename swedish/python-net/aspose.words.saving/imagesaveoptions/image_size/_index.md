---
title: ImageSaveOptions.image_size property
linktitle: image_size property
articleTitle: image_size property
second_title: Aspose.Words for Python
description: "ImageSaveOptions.image_size property. Gets or sets the size of a generated image in pixels."
type: docs
weight: 60
url: /sv/python-net/aspose.words.saving/imagesaveoptions/image_size/
---

## ImageSaveOptions.image_size property

Gets or sets the size of a generated image in pixels.


```python
@property
def image_size(self) -> aspose.pydrawing.Size:
    ...

@image_size.setter
def image_size(self, value: aspose.pydrawing.Size):
    ...

```

### Remarks

This property has effect only when saving to raster image formats.

The default value is (0 x 0), which means that the size of the generated image will be calculated
according to the size of the image in points, the specified resolution and scale.




### Examples

Shows how to render every page of a document to a separate TIFF image.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
builder.writeln('Page 1.')
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.writeln('Page 2.')
builder.insert_image(IMAGE_DIR + 'Logo.jpg')
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.writeln('Page 3.')
# Skapa ett "ImageSaveOptions"‑objekt som vi kan skicka till dokumentets "save"‑metod
# för att ändra hur den metoden renderar dokumentet till en bild.
options = aw.saving.ImageSaveOptions(aw.SaveFormat.TIFF)
for i in range(doc.page_count):
    # Ställ in egenskapen "page_set" till numret på den första sidan från
    # vilken vi ska börja rendera dokumentet från.
    options.page_set = aw.saving.PageSet(i)
    options.vertical_resolution = 600
    options.horizontal_resolution = 600
    options.image_size = aspose.pydrawing.Size(2325, 5325)
    doc.save(ARTIFACTS_DIR + f'ImageSaveOptions.page_by_page.{i + 1}.tiff', options)
```

### See Also

* module [aspose.words.saving](../../)
* class [ImageSaveOptions](../)

