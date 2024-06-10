---
title: ImageSaveOptions constructor
linktitle: ImageSaveOptions constructor
articleTitle: ImageSaveOptions constructor
second_title: Aspose.Words for Python
description: "ImageSaveOptions constructor. Initializes a new instance of this class that can be used to save rendered images in the [SaveFormat.TIFF](../../../aspose.words/saveformat/#TIFF), [SaveFormat.PNG](../../../aspose.words/saveformat/#PNG), [SaveFormat.BMP](../../../aspose.words/saveformat/#BMP), [SaveFormat.JPEG](../../../aspose.words/saveformat/#JPEG), [SaveFormat.EMF](../../../aspose.words/saveformat/#EMF), [SaveFormat.EPS](../../../aspose.words/saveformat/#EPS), [SaveFormat.WEB_P](../../../aspose.words/saveformat/#WEB_P) or [SaveFormat.SVG](../../../aspose.words/saveformat/#SVG) format."
type: docs
weight: 10
url: /python-net/aspose.words.saving/imagesaveoptions/__init__/
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
builder = aw.DocumentBuilder(doc)
builder.insert_image(IMAGE_DIR + 'Logo.jpg')
# Create an "ImageSaveOptions" object which we can pass to the document's "save" method
# to modify the way in which that method renders the document into an image.
image_options = aw.saving.ImageSaveOptions(aw.SaveFormat.JPEG)
# Set the "jpeg_quality" property to "10" to use stronger compression when rendering the document.
# This will reduce the file size of the document, but the image will display more prominent compression artifacts.
image_options.jpeg_quality = 10
doc.save(ARTIFACTS_DIR + 'ImageSaveOptions.jpeg_quality.high_compression.jpg', image_options)
self.assertGreater(20000, os.path.getsize(ARTIFACTS_DIR + 'ImageSaveOptions.jpeg_quality.high_compression.jpg'))
# Set the "jpeg_quality" property to "100" to use weaker compression when rending the document.
# This will improve the quality of the image at the cost of an increased file size.
image_options.jpeg_quality = 100
doc.save(ARTIFACTS_DIR + 'ImageSaveOptions.jpeg_quality.high_quality.jpg', image_options)
self.assertLess(40000, os.path.getsize(ARTIFACTS_DIR + 'ImageSaveOptions.jpeg_quality.high_quality.jpg'))
```

### See Also

* module [aspose.words.saving](../../)
* class [ImageSaveOptions](../)

