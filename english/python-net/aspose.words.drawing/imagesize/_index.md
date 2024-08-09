---
title: ImageSize class
linktitle: ImageSize class
articleTitle: ImageSize class
second_title: Aspose.Words for Python
description: "aspose.words.drawing.ImageSize class. Contains information about image size and resolution"
type: docs
weight: 210
url: /python-net/aspose.words.drawing/imagesize/
---

## ImageSize class

Contains information about image size and resolution.
To learn more, visit the [Working with Images](https://docs.aspose.com/words/python-net/working-with-images/) documentation article.




### Constructors
| Name | Description |
| --- | --- |
| [ImageSize(width_pixels, height_pixels)](./__init__/#int_int) | Initializes width and height to the given values in pixels. Initializes resolution to 96 dpi. |
| [ImageSize(width_pixels, height_pixels, horizontal_resolution, vertical_resolution)](./__init__/#int_int_float_float) | Initializes width, height and resolution to the given values. |

### Properties

| Name | Description |
| --- | --- |
| [height_pixels](./height_pixels/) | Gets the height of the image in pixels. |
| [height_points](./height_points/) | Gets the height of the image in points. 1 point is 1/72 inch. |
| [horizontal_resolution](./horizontal_resolution/) | Gets the horizontal resolution in DPI. |
| [vertical_resolution](./vertical_resolution/) | Gets the vertical resolution in DPI. |
| [width_pixels](./width_pixels/) | Gets the width of the image in pixels. |
| [width_points](./width_points/) | Gets the width of the image in points. 1 point is 1/72 inch. |

### Examples

Shows how to resize a shape with an image.

```python
# When we insert an image using the "insert_image" method, the builder scales the shape that displays the image so that,
# when we view the document using 100% zoom in Microsoft Word, the shape displays the image in its actual size.
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
shape = builder.insert_image(IMAGE_DIR + 'Logo.jpg')
# A 400x400 image will create an ImageData object with an image size of 300x300pt.
image_size = shape.image_data.image_size
self.assertEqual(300.0, image_size.width_points)
self.assertEqual(300.0, image_size.height_points)
# If a shape's dimensions match the image data's dimensions,
# then the shape is displaying the image in its original size.
self.assertEqual(300.0, shape.width)
self.assertEqual(300.0, shape.height)
# Reduce the overall size of the shape by 50%.
shape.width *= 0.5
# Scaling factors apply to both the width and the height at the same time to preserve the shape's proportions.
self.assertEqual(150.0, shape.width)
self.assertEqual(150.0, shape.height)
# When we resize the shape, the size of the image data remains the same.
self.assertEqual(300.0, image_size.width_points)
self.assertEqual(300.0, image_size.height_points)
# We can reference the image data dimensions to apply a scaling based on the size of the image.
shape.width = image_size.width_points * 1.1
self.assertEqual(330.0, shape.width)
self.assertEqual(330.0, shape.height)
doc.save(ARTIFACTS_DIR + 'Image.scale_image.docx')
```

### See Also

* module [aspose.words.drawing](../)
* property [ImageData.image_size](../imagedata/image_size/)

