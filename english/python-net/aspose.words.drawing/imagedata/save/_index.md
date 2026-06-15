---
title: ImageData.save method
linktitle: save method
articleTitle: save method
second_title: Aspose.Words for Python
description: "aspose.words.drawing.ImageData.save method"
type: docs
weight: 200
url: /python-net/aspose.words.drawing/imagedata/save/
---

## save(stream) {#bytesio}

Saves the image into the specified stream.


```python
def save(self, stream: io.BytesIO):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| stream | io.BytesIO | The stream where to save the image to. |

### Remarks

Is it the responsibility of the caller to dispose the stream object.




## save(file_name) {#str}

Saves the image into a file.


```python
def save(self, file_name: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| file_name | str | The file name where to save the image. |

## Examples

Shows how to save all images from a document to the file system.

```python
img_source_doc = aw.Document(file_name=MY_DIR + 'Images.docx')
# Get all shape nodes and filter those that have images
shapes_with_images = []
for node in img_source_doc.get_child_nodes(aw.NodeType.SHAPE, True):
    shape = node.as_shape()
    if shape.has_image:
        shapes_with_images.append(shape)
# Go through each shape and save its image.
shape_index = 0
while shape_index < len(shapes_with_images):
    image_data = shapes_with_images[shape_index].image_data
    image_data.save(ARTIFACTS_DIR + f'Drawing.SaveAllImages.{shape_index + 1}.{image_data.image_type}')
    shape_index += 1
```

## See Also

* module [aspose.words.drawing](../../)
* class [ImageData](../)

