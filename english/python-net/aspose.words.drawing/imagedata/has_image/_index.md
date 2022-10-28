---
title: has_image property
second_title: Aspose.Words for Python via .NET API Reference
description: "Returns ``True`` if the shape has image bytes or links an image."
type: docs
weight: 110
url: /python-net/aspose.words.drawing/imagedata/has_image/
---

## ImageData.has_image property

Returns ``True`` if the shape has image bytes or links an image.



### Examples

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

### See Also

* module [aspose.words.drawing](../../)
* class [ImageData](../)

