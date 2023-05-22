---
title: FileFormatUtil.image_type_to_extension method
linktitle: image_type_to_extension method
articleTitle: image_type_to_extension method
second_title: Aspose.Words for Python
description: "FileFormatUtil.image_type_to_extension method. Converts an Aspose.Words image type enumerated value into a file extension"
type: docs
weight: 50
url: /python-net/aspose.words/fileformatutil/image_type_to_extension/
---

## image_type_to_extension(image_type) {#imagetype}

Converts an Aspose.Words image type enumerated value into a file extension. The returned extension is a lower-case string with a leading dot.


```python
def image_type_to_extension(self, image_type: aspose.words.drawing.ImageType):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| image_type | [ImageType](../../../aspose.words.drawing/imagetype/) |  |

### Exceptions

| exception | condition |
| --- | --- |
| System.ArgumentException | Throws when cannot convert. |

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

* module [aspose.words](../../)
* class [FileFormatUtil](../)

