---
title: height_pixels property
second_title: Aspose.Words for Python via .NET API Reference
description: "Gets the height of the image in pixels."
type: docs
weight: 20
url: /python-net/aspose.words.drawing/imagesize/height_pixels/
---

## ImageSize.height_pixels property

Gets the height of the image in pixels.


### Examples

Shows how to read the properties of an image in a shape.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

# Insert a shape into the document which contains an image taken from our local file system.
shape = builder.insert_image(IMAGE_DIR + "Logo.jpg")

# If the shape contains an image, its "image_data" property will be valid,
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

doc.save(ARTIFACTS_DIR + "Drawing.image_size.docx")
```

### See Also

* module [aspose.words.drawing](../../)
* class [ImageSize](../)

