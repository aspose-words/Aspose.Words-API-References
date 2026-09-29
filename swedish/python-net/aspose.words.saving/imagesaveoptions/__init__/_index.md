---
title: ImageSaveOptions constructor
linktitle: ImageSaveOptions constructor
articleTitle: ImageSaveOptions constructor
second_title: Aspose.Words for Python
description: "ImageSaveOptions constructor. Initializes a new instance of this class that can be used to save rendered images in the [SaveFormat.TIFF](../../../aspose.words/saveformat/#TIFF), [SaveFormat.PNG](../../../aspose.words/saveformat/#PNG), [SaveFormat.BMP](../../../aspose.words/saveformat/#BMP), [SaveFormat.JPEG](../../../aspose.words/saveformat/#JPEG), [SaveFormat.EMF](../../../aspose.words/saveformat/#EMF), [SaveFormat.EPS](../../../aspose.words/saveformat/#EPS), [SaveFormat.WEB_P](../../../aspose.words/saveformat/#WEB_P) or [SaveFormat.SVG](../../../aspose.words/saveformat/#SVG) format."
type: docs
weight: 10
url: /sv/python-net/aspose.words.saving/imagesaveoptions/__init__/
---

## ImageSaveOptions(save_format) {#saveformat}

Initializes a new instance of this class that can be used to save rendered images in the
[SaveFormat.TIFF](../../../aspose.words/saveformat/#TIFF), [SaveFormat.PNG](../../../aspose.words/saveformat/#PNG), [SaveFormat.BMP](../../../aspose.words/saveformat/#BMP),
[SaveFormat.JPEG](../../../aspose.words/saveformat/#JPEG), [SaveFormat.EMF](../../../aspose.words/saveformat/#EMF), [SaveFormat.EPS](../../../aspose.words/saveformat/#EPS),
[SaveFormat.WEB_P](../../../aspose.words/saveformat/#WEB_P) or [SaveFormat.SVG](../../../aspose.words/saveformat/#SVG) format.



```python
def __init__(self, save_format: aspose.words.SaveFormat):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| save_format | [SaveFormat](../../../aspose.words/saveformat/) | Can be [SaveFormat.TIFF](../../../aspose.words/saveformat/#TIFF), [SaveFormat.PNG](../../../aspose.words/saveformat/#PNG), [SaveFormat.BMP](../../../aspose.words/saveformat/#BMP), [SaveFormat.JPEG](../../../aspose.words/saveformat/#JPEG), [SaveFormat.EMF](../../../aspose.words/saveformat/#EMF), [SaveFormat.EPS](../../../aspose.words/saveformat/#EPS) [SaveFormat.WEB_P](../../../aspose.words/saveformat/#WEB_P) or [SaveFormat.SVG](../../../aspose.words/saveformat/#SVG) format. |

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
* class [ImageSaveOptions](../)

