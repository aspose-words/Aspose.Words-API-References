---
title: ImageData.to_stream method
linktitle: to_stream method
articleTitle: to_stream method
second_title: Aspose.Words for Python
description: "ImageData.to_stream method. Creates and returns a stream that contains the image bytes."
type: docs
weight: 230
url: /it/python-net/aspose.words.drawing/imagedata/to_stream/
---

## to_stream() {#default}

Creates and returns a stream that contains the image bytes.


```python
def to_stream(self):
    ...
```

### Remarks

If the image bytes are stored in the shape, creates and returns a io.BytesIO object.

If the image is linked and stored in a file, opens the file and returns a io.BytesIO object.

If the image is linked and stored in an external URL, downloads the file and returns a io.BytesIO object.

Is it the responsibility of the caller to dispose the stream object.




### Examples

Shows how to create an image file from a shape's raw image data.

```python
img_source_doc = aw.Document(file_name=MY_DIR + 'Images.docx')
img_shape = img_source_doc.get_child(aw.NodeType.SHAPE, 0, True).as_shape()
self.assertTrue(img_shape.has_image)
# ToByteArray() restituisce l'array memorizzato nella proprietà ImageBytes.
assert img_shape.image_data.image_bytes == img_shape.image_data.to_byte_array()
# Salva i dati immagine della forma in un file immagine nel file system locale.
with img_shape.image_data.to_stream() as img_stream:
    with system_helper.io.FileStream(ARTIFACTS_DIR + 'Drawing.GetDataFromImage.png', system_helper.io.FileMode.CREATE, system_helper.io.FileAccess.READ_WRITE) as out_stream:
        out_stream.write(img_stream.read())
```

### See Also

* module [aspose.words.drawing](../../)
* class [ImageData](../)

