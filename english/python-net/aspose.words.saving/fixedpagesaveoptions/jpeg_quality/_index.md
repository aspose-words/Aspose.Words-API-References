---
title: jpeg_quality property
second_title: Aspose.Words for Python via .NET API Reference
description: "Gets or sets a value determining the quality of the JPEG images inside Html document."
type: docs
weight: 20
url: /python-net/aspose.words.saving/fixedpagesaveoptions/jpeg_quality/
---

## FixedPageSaveOptions.jpeg_quality property

Gets or sets a value determining the quality of the JPEG images inside Html document.

Has effect only when a document contains JPEG images.

Use this property to get or set the quality of the images inside a document when saving in fixed page format.
The value may vary from 0 to 100 where 0 means worst quality but maximum compression and 100
means best quality but minimum compression.

The default value is 95.




### Examples

Shows how to configure compression while saving a document as a JPEG.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
builder.insert_image(IMAGE_DIR + "Logo.jpg")

# Create an "ImageSaveOptions" object which we can pass to the document's "save" method
# to modify the way in which that method renders the document into an image.
image_options = aw.saving.ImageSaveOptions(aw.SaveFormat.JPEG)

# Set the "jpeg_quality" property to "10" to use stronger compression when rendering the document.
# This will reduce the file size of the document, but the image will display more prominent compression artifacts.
image_options.jpeg_quality = 10

doc.save(ARTIFACTS_DIR + "ImageSaveOptions.jpeg_quality.high_compression.jpg", image_options)

self.assertGreater(20000, os.path.getsize(ARTIFACTS_DIR + "ImageSaveOptions.jpeg_quality.high_compression.jpg"))

# Set the "jpeg_quality" property to "100" to use weaker compression when rending the document.
# This will improve the quality of the image at the cost of an increased file size.
image_options.jpeg_quality = 100

doc.save(ARTIFACTS_DIR + "ImageSaveOptions.jpeg_quality.high_quality.jpg", image_options)

self.assertLess(60000, os.path.getsize(ARTIFACTS_DIR + "ImageSaveOptions.jpeg_quality.high_quality.jpg"))
```

### See Also

* module [aspose.words.saving](../../)
* class [FixedPageSaveOptions](../)

