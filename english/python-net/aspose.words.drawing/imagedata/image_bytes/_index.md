---
title: ImageData.image_bytes property
linktitle: image_bytes property
articleTitle: image_bytes property
second_title: Aspose.Words for Python
description: "ImageData.image_bytes property. Gets or sets the raw bytes of the image stored in the shape."
type: docs
weight: 120
url: /python-net/aspose.words.drawing/imagedata/image_bytes/
---

## ImageData.image_bytes property

Gets or sets the raw bytes of the image stored in the shape.

Setting the value to ``None`` or an empty array will remove the image from the shape.

Returns ``None`` if the image is not stored in the document (e.g the image is probably linked in this case).




### Examples

Shows how to create an image file from a shape's raw image data.

```python
img_source_doc = aw.Document(MY_DIR + "Images.docx")

img_shape = img_source_doc.get_child(aw.NodeType.SHAPE, 0, True).as_shape()

self.assertTrue(img_shape.has_image)

# to_byte_array() returns the array stored in the "image_bytes" property.
self.assertEqual(img_shape.image_data.image_bytes, img_shape.image_data.to_byte_array())

# Save the shape's image data to an image file in the local file system.
with img_shape.image_data.to_stream() as img_stream:

    with open(ARTIFACTS_DIR + "Drawing.get_data_from_image.png", "wb") as out_stream:
        out_stream.write(img_stream.read())
```

### See Also

* module [aspose.words.drawing](../../)
* class [ImageData](../)
* method [ImageData.set_image()](../set_image/#str)
* method [ImageData.to_byte_array()](../to_byte_array/#default)
* method [ImageData.to_stream()](../to_stream/#default)
* method [ImageData.save()](../save/#str)

