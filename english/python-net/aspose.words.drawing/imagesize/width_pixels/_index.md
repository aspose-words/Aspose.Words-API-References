﻿---
title: ImageSize.width_pixels property
linktitle: width_pixels property
articleTitle: width_pixels property
second_title: Aspose.Words for Python
description: "ImageSize.width_pixels property. Gets the width of the image in pixels."
type: docs
weight: 60
url: /python-net/aspose.words.drawing/imagesize/width_pixels/
---

## ImageSize.width_pixels property

Gets the width of the image in pixels.


```python
@property
def width_pixels(self) -> int:
    ...

```

### Examples

Shows how to read the properties of an image in a shape.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Insert a shape into the document which contains an image taken from our local file system.
shape = builder.insert_image(file_name=IMAGE_DIR + 'Logo.jpg')
# If the shape contains an image, its ImageData property will be valid,
# and it will contain an ImageSize object.
image_size = shape.image_data.image_size
# The ImageSize object contains read-only information about the image within the shape.
self.assertEqual(400, image_size.height_pixels)
self.assertEqual(400, image_size.width_pixels)
delta = 0.05
self.assertAlmostEqual(95.98, image_size.horizontal_resolution, delta=delta)
self.assertAlmostEqual(95.98, image_size.vertical_resolution, delta=delta)
# We can base the size of the shape on the size of its image to avoid stretching the image.
shape.width = image_size.width_points * 2
shape.height = image_size.height_points * 2
doc.save(file_name=ARTIFACTS_DIR + 'Drawing.ImageSize.docx')
```

### See Also

* module [aspose.words.drawing](../../)
* class [ImageSize](../)

