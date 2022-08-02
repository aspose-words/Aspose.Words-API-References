---
title: source_full_name property
second_title: Aspose.Words for Python via .NET API Reference
description: "Gets or sets the path and name of the source file for the linked image."
type: docs
weight: 170
url: /python-net/aspose.words.drawing/imagedata/source_full_name/
---

## ImageData.source_full_name property

Gets or sets the path and name of the source file for the linked image.

The default value is an empty string.

If [ImageData.source_full_name](./) is not an empty string, the image is linked.




### Examples

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
* class [ImageData](../)

