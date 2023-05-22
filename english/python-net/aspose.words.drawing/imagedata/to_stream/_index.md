---
title: ImageData.to_stream method
linktitle: to_stream method
articleTitle: to_stream method
second_title: Aspose.Words for Python
description: "ImageData.to_stream method. Creates and returns a stream that contains the image bytes."
type: docs
weight: 220
url: /python-net/aspose.words.drawing/imagedata/to_stream/
---

## to_stream() {#default}

Creates and returns a stream that contains the image bytes.


```python
def to_stream(self):
    ...
```

If the image bytes are stored in the shape, creates and returns a System.IO.MemoryStream object.

If the image is linked and stored in a file, opens the file and returns a System.IO.FileStream object.

If the image is linked and stored in an external URL, downloads the file and returns a System.IO.MemoryStream object.

Is it the responsibility of the caller to dispose the stream object.




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

