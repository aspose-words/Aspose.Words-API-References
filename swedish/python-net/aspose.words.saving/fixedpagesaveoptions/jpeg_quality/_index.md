---
title: FixedPageSaveOptions.jpeg_quality property
linktitle: jpeg_quality property
articleTitle: jpeg_quality property
second_title: Aspose.Words for Python
description: "FixedPageSaveOptions.jpeg_quality property. Gets or sets a value determining the quality of the JPEG images inside Html document."
type: docs
weight: 20
url: /sv/python-net/aspose.words.saving/fixedpagesaveoptions/jpeg_quality/
---

## FixedPageSaveOptions.jpeg_quality property

Gets or sets a value determining the quality of the JPEG images inside Html document.


```python
@property
def jpeg_quality(self) -> int:
    ...

@jpeg_quality.setter
def jpeg_quality(self, value: int):
    ...

```

### Remarks

Has effect only when a document contains JPEG images.

Use this property to get or set the quality of the images inside a document when saving in fixed page format.
The value may vary from 0 to 100 where 0 means worst quality but maximum compression and 100
means best quality but minimum compression.

The default value is 95.




### Examples

Shows how to configure compression while saving a document as a JPEG.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.insert_image(file_name=IMAGE_DIR + 'Logo.jpg')
# Skapa ett "ImageSaveOptions"‑objekt som vi kan skicka till dokumentets "Save"‑metod
# för att ändra hur den metoden renderar dokumentet till en bild.
image_options = aw.saving.ImageSaveOptions(aw.SaveFormat.JPEG)
# Ställ in egenskapen "JpegQuality" till "10" för att använda starkare komprimering vid rendering av dokumentet.
# Detta kommer att minska filstorleken på dokumentet, men bilden kommer att visa mer framträdande komprimeringsartefakter.
image_options.jpeg_quality = 10
doc.save(file_name=ARTIFACTS_DIR + 'ImageSaveOptions.JpegQuality.HighCompression.jpg', save_options=image_options)
# Ställ in egenskapen "JpegQuality" till "100" för att använda svagare komprimering när dokumentet renderas.
# Detta kommer att förbättra bildens kvalitet på bekostnad av en ökad filstorlek.
image_options.jpeg_quality = 100
doc.save(file_name=ARTIFACTS_DIR + 'ImageSaveOptions.JpegQuality.HighQuality.jpg', save_options=image_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [FixedPageSaveOptions](../)

