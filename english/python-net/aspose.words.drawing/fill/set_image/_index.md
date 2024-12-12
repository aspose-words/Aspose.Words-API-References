---
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
builder = aw.DocumentBuilder(doc=doc)
# There are several ways of setting image.
shape = builder.insert_shape(shape_type=aw.drawing.ShapeType.RECTANGLE, width=80, height=80)
# 1 -  Using a local system filename:
shape.fill.set_image(file_name=IMAGE_DIR + 'Logo.jpg')
doc.save(file_name=ARTIFACTS_DIR + 'Shape.FillImage.FileName.docx')
# 2 -  Load a file into a byte array:
shape.fill.set_image(image_bytes=system_helper.io.File.read_all_bytes(IMAGE_DIR + 'Logo.jpg'))
doc.save(file_name=ARTIFACTS_DIR + 'Shape.FillImage.ByteArray.docx')
# 3 -  From a stream:
with system_helper.io.FileStream(IMAGE_DIR + 'Logo.jpg', system_helper.io.FileMode.OPEN) as stream:
    shape.fill.set_image(stream=stream)
doc.save(file_name=ARTIFACTS_DIR + 'Shape.FillImage.Stream.docx')
```

## See Also

* module [aspose.words.drawing](../../)
* class [Fill](../)

