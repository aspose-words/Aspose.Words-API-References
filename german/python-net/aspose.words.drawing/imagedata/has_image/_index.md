---
title: ImageData.has_image property
linktitle: has_image property
articleTitle: has_image property
second_title: Aspose.Words for Python
description: "ImageData.has_image property. Returns ``True`` if the shape has image bytes or links an image."
type: docs
weight: 110
url: /de/python-net/aspose.words.drawing/imagedata/has_image/
---

## ImageData.has_image property

Returns ``True`` if the shape has image bytes or links an image.



```python
@property
def has_image(self) -> bool:
    ...

```

### Examples

Shows how to save all images from a document to the file system.

```python
img_source_doc = aw.Document(file_name=MY_DIR + 'Images.docx')
# Alle Formknoten abrufen und diejenigen filtern, die Bilder enthalten
shapes_with_images = []
for node in img_source_doc.get_child_nodes(aw.NodeType.SHAPE, True):
    shape = node.as_shape()
    if shape.has_image:
        shapes_with_images.append(shape)
# Jede Form durchgehen und ihr Bild speichern.
shape_index = 0
while shape_index < len(shapes_with_images):
    image_data = shapes_with_images[shape_index].image_data
    image_data.save(ARTIFACTS_DIR + f'Drawing.SaveAllImages.{shape_index + 1}.{image_data.image_type}')
    shape_index += 1
```

### See Also

* module [aspose.words.drawing](../../)
* class [ImageData](../)

