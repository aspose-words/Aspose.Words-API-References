---
title: Shape.has_image property
linktitle: has_image property
articleTitle: has_image property
second_title: Aspose.Words for Python
description: "Shape.has_image property. Returns ``True`` if the shape has image bytes or links an image."
type: docs
weight: 80
url: /python-net/aspose.words.drawing/shape/has_image/
---

## Shape.has_image property

Returns ``True`` if the shape has image bytes or links an image.



```python
@property
def has_image(self) -> bool:
    ...

```

### Examples

Shows how to extract images from a document, and save them to the local file system as individual files.

```python
doc = aw.Document(MY_DIR + "Images.docx")

# Get the collection of shapes from the document,
# and save the image data of every shape with an image as a file to the local file system.
shapes = doc.get_child_nodes(aw.NodeType.SHAPE, True)

self.assertEqual(9, len([s for s in shapes if s.as_shape().has_image]))

image_index = 0
for shape in shapes:
    shape = shape.as_shape()

    if shape.has_image:

        # The image data of shapes may contain images of many possible image formats.
        # We can determine a file extension for each image automatically, based on its format.
        image_file_name = f"File.extract_images.{image_index}{aw.FileFormatUtil.image_type_to_extension(shape.image_data.image_type)}"
        shape.image_data.save(ARTIFACTS_DIR + image_file_name)
        image_index += 1
```

Shows how to delete all shapes with images from a document.

```python
doc = aw.Document(MY_DIR + "Images.docx")
shapes = doc.get_child_nodes(aw.NodeType.SHAPE, True)

self.assertEqual(9, len([node for node in shapes if node.as_shape().has_image]))

for node in shapes:
    shape = node.as_shape()
    if shape.has_image:
        shape.remove()

self.assertEqual(0, len([node for node in shapes if node.as_shape().has_image]))
```

### See Also

* module [aspose.words.drawing](../../)
* class [Shape](../)

