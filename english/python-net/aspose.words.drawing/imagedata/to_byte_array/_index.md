---
title: ImageData.to_byte_array method
linktitle: to_byte_array method
articleTitle: to_byte_array method
second_title: Aspose.Words for Python
description: "ImageData.to_byte_array method. Returns image bytes for any image regardless whether the image is stored or linked."
type: docs
weight: 220
url: /python-net/aspose.words.drawing/imagedata/to_byte_array/
---

## to_byte_array() {#default}

Returns image bytes for any image regardless whether the image is stored or linked.


```python
def to_byte_array(self):
    ...
```

### Remarks

If the image is linked, downloads the image every time it is called.




### Returns




### Examples

Shows how to create an image file from a shape's raw image data.

```python
img_source_doc = aw.Document(file_name=MY_DIR + 'Images.docx')
img_shape = img_source_doc.get_child(aw.NodeType.SHAPE, 0, True).as_shape()
self.assertTrue(img_shape.has_image)
# ToByteArray() returns the array stored in the ImageBytes property.
assert img_shape.image_data.image_bytes == img_shape.image_data.to_byte_array()
# Save the shape's image data to an image file in the local file system.
with img_shape.image_data.to_stream() as img_stream:
    with system_helper.io.FileStream(ARTIFACTS_DIR + 'Drawing.GetDataFromImage.png', system_helper.io.FileMode.CREATE, system_helper.io.FileAccess.READ_WRITE) as out_stream:
        out_stream.write(img_stream.read())
```

### See Also

* module [aspose.words.drawing](../../)
* class [ImageData](../)
* property [ImageData.image_bytes](../image_bytes/)

