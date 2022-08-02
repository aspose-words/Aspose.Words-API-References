---
title: scale property
second_title: Aspose.Words for Python via .NET API Reference
description: "Gets or sets the scale factor expressed as a fraction of the image"
type: docs
weight: 30
url: /python-net/aspose.words/imagewatermarkoptions/scale/
---

## ImageWatermarkOptions.scale property

Gets or sets the scale factor expressed as a fraction of the image. The default value is 0 - auto.

Valid values range from 0 to 65.5 inclusive.

Auto scale means that the watermark will be scaled to its max width and max height relative to
the page margins.



:raises System.ArgumentOutOfRangeException: Throws when argument was out of the range of valid values.
                                            

### Examples

Shows how to create a watermark from an image in the local file system.

```python
doc = aw.Document()

# Modify the image watermark's appearance with an ImageWatermarkOptions object,
# then pass it while creating a watermark from an image file.
image_watermark_options = aw.ImageWatermarkOptions()
image_watermark_options.scale = 5
image_watermark_options.is_washout = False

doc.watermark.set_image(drawing.Image.from_file(IMAGE_DIR + "Logo.jpg"), image_watermark_options)

doc.save(ARTIFACTS_DIR + "Document.image_watermark.docx")
```

### See Also

* module [aspose.words](../../)
* class [ImageWatermarkOptions](../)

