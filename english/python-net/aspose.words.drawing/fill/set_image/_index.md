﻿---
title: Fill.set_image method
linktitle: set_image method
articleTitle: set_image method
second_title: Aspose.Words for Python
description: "aspose.words.drawing.Fill.set_image method"
type: docs
weight: 250
url: /python-net/aspose.words.drawing/fill/set_image/
---

## set_image(file_name) {#str}

Changes the fill type to single image.


```python
def set_image(self, file_name: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| file_name | str | The path to the image file. |

## set_image(stream) {#bytesio}

Changes the fill type to single image.


```python
def set_image(self, stream: io.BytesIO):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| stream | io.BytesIO | The stream that contains the image bytes. |

## set_image(image_bytes) {#bytes}

Changes the fill type to single image.


```python
def set_image(self, image_bytes: bytes):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| image_bytes | bytes | The image bytes array. |

## Examples

Shows how to set shape fill type as image.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
# There are several ways of setting image.
shape = builder.insert_shape(aw.drawing.ShapeType.RECTANGLE, 80, 80)
# 1 -  Using a local system filename:
shape.fill.set_image(IMAGE_DIR + 'Logo.jpg')
doc.save(ARTIFACTS_DIR + 'Shape.fill_image.file_name.docx')
# 2 -  Load a file into a byte array:
with open(IMAGE_DIR + 'Logo.jpg', 'rb') as stream:
    shape.fill.set_image(stream.read())
doc.save(ARTIFACTS_DIR + 'Shape.fill_image.byte_array.docx')
# 3 -  From a stream:
with open(IMAGE_DIR + 'Logo.jpg', 'rb') as stream:
    shape.fill.set_image(stream)
doc.save(ARTIFACTS_DIR + 'Shape.fill_image.stream.docx')
```

## See Also

* module [aspose.words.drawing](../../)
* class [Fill](../)

