---
title: save method
second_title: Aspose.Words for Python via .NET API Reference
description: "aspose.words.rendering.NodeRendererBase.save method"
type: docs
weight: 70
url: /python-net/aspose.words.rendering/noderendererbase/save/
---

## save(file_name, save_options) {#str_imagesaveoptions}

Renders the shape into an image and saves into a file.


```python
def save(self, file_name: str, save_options: aspose.words.saving.ImageSaveOptions):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| file_name | str |  |
| save_options | [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/) |  |

## save(stream, save_options) {#bytesio_imagesaveoptions}

Renders the shape into an image and saves into a stream.


```python
def save(self, stream: BytesIO, save_options: aspose.words.saving.ImageSaveOptions):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| stream | BytesIO |  |
| save_options | [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/) |  |

## Examples

Shows how to render an Office Math object into an image file in the local file system.

```python
doc = aw.Document(MY_DIR + "Office math.docx")

math = doc.get_child(aw.NodeType.OFFICE_MATH, 0, True).as_office_math()

# Create an "ImageSaveOptions" object to pass to the node renderer's "save" method to modify
# how it renders the OfficeMath node into an image.
save_options = aw.saving.ImageSaveOptions(aw.SaveFormat.PNG)

# Set the "scale" property to 5 to render the object to five times its original size.
save_options.scale = 5

math.get_math_renderer().save(ARTIFACTS_DIR + "Shape.render_office_math.png", save_options)
```

Shows how to use a shape renderer to export shapes to files in the local file system.

```python
doc = aw.Document(MY_DIR + "Various shapes.docx")
shapes = [node.as_shape() for node in doc.get_child_nodes(aw.NodeType.SHAPE, True)]

self.assertEqual(7, len(shapes))

# There are 7 shapes in the document, including one group shape with 2 child shapes.
# We will render every shape to an image file in the local file system
# while ignoring the group shapes since they have no appearance.
# This will produce 6 image files.
for shape in doc.get_child_nodes(aw.NodeType.SHAPE, True):
    shape = shape.as_shape()
    renderer = shape.get_shape_renderer()
    options = aw.saving.ImageSaveOptions(aw.SaveFormat.PNG)
    renderer.save(ARTIFACTS_DIR + "Shape.render_all_shapes." + shape.name + ".png", options)
```

## See Also

* module [aspose.words.rendering](../../)
* class [NodeRendererBase](../)

