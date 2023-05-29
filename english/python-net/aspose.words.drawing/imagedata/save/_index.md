---
title: ImageData.save method
linktitle: save method
articleTitle: save method
second_title: Aspose.Words for Python
description: "aspose.words.drawing.ImageData.save method"
type: docs
weight: 190
url: /python-net/aspose.words.drawing/imagedata/save/
---

## save(stream) {#bytesio}

Saves the image into the specified stream.


```python
def save(self, stream: BytesIO):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| stream | BytesIO |  |

Is it the responsibility of the caller to dispose the stream object.




## save(file_name) {#str}

Saves the image into a file.


```python
def save(self, file_name: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| file_name | str |  |

## Examples

Shows how to save all images from a document to the file system.

```python
img_source_doc = aw.Document(MY_DIR + "Images.docx")

# Shapes with the "has_image" flag set store and display all the document's images.
shapes_with_images = [node.as_shape() for node in img_source_doc.get_child_nodes(aw.NodeType.SHAPE, True) if node.as_shape().has_image]

# Go through each shape and save its image.
format_converter = drawing.ImageFormatConverter()

for shape_index, shape in enumerate(shapes_with_images):
    image_data = shape.image_data
    format = image_data.to_image().raw_format
    file_extension = format_converter.convert_to_string(format)

    with open(ARTIFACTS_DIR + f"Drawing.save_all_images.{shape_index}.{file_extension}", "wb") as file_stream:
        file_stream.write(file_stream)
```

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

## See Also

* module [aspose.words.drawing](../../)
* class [ImageData](../)

