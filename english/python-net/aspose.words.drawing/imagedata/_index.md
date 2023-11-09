---
title: ImageData class
linktitle: ImageData class
articleTitle: ImageData class
second_title: Aspose.Words for Python
description: "aspose.words.drawing.ImageData class. Defines an image for a shape"
type: docs
weight: 170
url: /python-net/aspose.words.drawing/imagedata/
---

## ImageData class

Defines an image for a shape.
To learn more, visit the [Working with Images](https://docs.aspose.com/words/python-net/working-with-images/) documentation article.




### Remarks

Use the [Shape.image_data](../shape/image_data/) property to access and modify the image inside a shape.
You do not create instances of the [ImageData](./) class directly.

An image can be stored inside a shape, linked to external file or both (linked and stored in the document).

Regardless of whether the image is stored inside the shape or linked, you can always access the actual
image using the [ImageData.to_byte_array()](./to_byte_array/#default), [ImageData.to_stream()](./to_stream/#default) or [ImageData.save()](./save/#str) methods.
If the image is stored inside the shape, you can also directly access it using the [ImageData.image_bytes](./image_bytes/) property.

To store an image inside a shape use the [ImageData.set_image()](./set_image/#str) method. To link an image to a shape, set the [ImageData.source_full_name](./source_full_name/) property.




### Properties

| Name | Description |
| --- | --- |
| [bi_level](./bi_level/) | Determines whether an image will be displayed in black and white. |
| [borders](./borders/) | Gets the collection of borders of the image. Borders only have effect for inline images. |
| [brightness](./brightness/) | Gets or sets the brightness of the picture. The value for this property must be a number from 0.0 (dimmest) to 1.0 (brightest). |
| [chroma_key](./chroma_key/) | Defines the color value of the image that will be treated as transparent. |
| [contrast](./contrast/) | Gets or sets the contrast for the specified picture. The value for this property must be a number from 0.0 (the least contrast) to 1.0 (the greatest contrast). |
| [crop_bottom](./crop_bottom/) | Defines the fraction of picture removal from the bottom side. |
| [crop_left](./crop_left/) | Defines the fraction of picture removal from the left side. |
| [crop_right](./crop_right/) | Defines the fraction of picture removal from the right side. |
| [crop_top](./crop_top/) | Defines the fraction of picture removal from the top side. |
| [gray_scale](./gray_scale/) | Determines whether a picture will display in grayscale mode. |
| [has_image](./has_image/) | Returns ``True`` if the shape has image bytes or links an image. |
| [image_bytes](./image_bytes/) | Gets or sets the raw bytes of the image stored in the shape. |
| [image_size](./image_size/) | Gets the information about image size and resolution. |
| [image_type](./image_type/) | Gets the type of the image. |
| [is_link](./is_link/) | Returns ``True`` if the image is linked to the shape (when [ImageData.source_full_name](./source_full_name/) is specified). |
| [is_link_only](./is_link_only/) | Returns ``True`` if the image is linked and not stored in the document. |
| [source_full_name](./source_full_name/) | Gets or sets the path and name of the source file for the linked image. |
| [title](./title/) | Defines the title of an image. |

### Methods

| Name | Description |
| --- | --- |
|[ fit_image_to_shape()](./fit_image_to_shape/#default) | Fits the image data to Shape frame so that the aspect ratio of the image data matches the aspect ratio of Shape frame. |
|[ save(stream)](./save/#bytesio) | Saves the image into the specified stream. |
|[ save(file_name)](./save/#str) | Saves the image into a file. |
|[ set_image(stream)](./set_image/#bytesio) | Sets the image that the shape displays. |
|[ set_image(file_name)](./set_image/#str) | Sets the image that the shape displays. |
|[ to_byte_array()](./to_byte_array/#default) | Returns image bytes for any image regardless whether the image is stored or linked. |
|[ to_stream()](./to_stream/#default) | Creates and returns a stream that contains the image bytes. |

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

Shows how to insert a linked image into a document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

image_file_name = IMAGE_DIR + "Windows MetaFile.wmf"

# Below are two ways of applying an image to a shape so that it can display it.
# 1 -  Set the shape to contain the image.
shape = aw.drawing.Shape(builder.document, aw.drawing.ShapeType.IMAGE)
shape.wrap_type = aw.drawing.WrapType.INLINE
shape.image_data.set_image(image_file_name)

builder.insert_node(shape)

doc.save(ARTIFACTS_DIR + "Image.create_linked_image.embedded.docx")

# Every image that we store in shape will increase the size of our document.
self.assertLess(70000, os.path.getsize(ARTIFACTS_DIR + "Image.create_linked_image.embedded.docx"))

doc.first_section.body.first_paragraph.remove_all_children()

# 2 -  Set the shape to link to an image file in the local file system.
shape = aw.drawing.Shape(builder.document, aw.drawing.ShapeType.IMAGE)
shape.wrap_type = aw.drawing.WrapType.INLINE
shape.image_data.source_full_name = image_file_name

builder.insert_node(shape)
doc.save(ARTIFACTS_DIR + "Image.create_linked_image.linked.docx")

# Linking to images will save space and result in a smaller document.
# However, the document can only display the image correctly while
# the image file is present at the location that the shape's "source_full_name" property points to.
self.assertGreater(10000, os.path.getsize(ARTIFACTS_DIR + "Image.create_linked_image.linked.docx"))
```

### See Also

* module [aspose.words.drawing](../)

