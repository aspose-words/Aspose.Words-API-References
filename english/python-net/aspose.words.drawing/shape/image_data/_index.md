---
title: image_data property
second_title: Aspose.Words for Python via .NET API Reference
description: "Provides access to the image of the shape"
type: docs
weight: 110
url: /python-net/aspose.words.drawing/shape/image_data/
---

## Shape.image_data property

Provides access to the image of the shape.
Returns null if the shape cannot have an image.


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

* module [aspose.words.drawing](../../)
* class [Shape](../)

