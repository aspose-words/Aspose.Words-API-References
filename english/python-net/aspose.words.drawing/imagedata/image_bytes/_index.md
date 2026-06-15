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


```python
@property
def image_bytes(self) -> bytes:
    ...

@image_bytes.setter
def image_bytes(self, value: bytes):
    ...

```

### Remarks

Setting the value to ``None`` or an empty array will remove the image from the shape.

Returns``None`` if the image is not stored in the document (e.g the image is probably linked in this case).




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
* method [ImageData.to_byte_array()](../to_byte_array/#default)
* method [ImageData.to_stream()](../to_stream/#default)
* method [ImageData.save()](../save/#str)

