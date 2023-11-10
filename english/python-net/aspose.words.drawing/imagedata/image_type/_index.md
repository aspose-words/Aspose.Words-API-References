---
title: ImageData.image_type property
linktitle: image_type property
articleTitle: image_type property
second_title: Aspose.Words for Python
description: "ImageData.image_type property. Gets the type of the image."
type: docs
weight: 140
url: /python-net/aspose.words.drawing/imagedata/image_type/
---

## ImageData.image_type property

Gets the type of the image.


```python
@property
def image_type(self) -> aspose.words.drawing.ImageType:
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

### See Also

* module [aspose.words.drawing](../../)
* class [ImageData](../)

