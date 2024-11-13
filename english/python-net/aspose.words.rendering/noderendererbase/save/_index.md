---
title: NodeRendererBase.save method
linktitle: save method
articleTitle: save method
second_title: Aspose.Words for Python
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
| file_name | str | The name for the image file. If a file with the specified name already exists, the existing file is overwritten. |
| save_options | [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/) | Specifies the options that control how the shape is rendered and saved. Can be ``None``. |

## save(file_name, save_options) {#str_svgsaveoptions}

Renders the shape into an SVG image and saves into a file.


```python
def save(self, file_name: str, save_options: aspose.words.saving.SvgSaveOptions):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| file_name | str | The name for the image file. If a file with the specified name already exists, the existing file is overwritten. |
| save_options | [SvgSaveOptions](../../../aspose.words.saving/svgsaveoptions/) | Specifies the options that control how the shape is rendered and saved. Can be ``None``. |

## save(stream, save_options) {#bytesio_imagesaveoptions}

Renders the shape into an image and saves into a stream.


```python
def save(self, stream: io.BytesIO, save_options: aspose.words.saving.ImageSaveOptions):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| stream | io.BytesIO | The stream where to save the image of the shape. |
| save_options | [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/) | Specifies the options that control how the shape is rendered and saved. Can be ``None``. If this is ``None``, the image will be saved in the PNG format. |

## save(stream, save_options) {#bytesio_svgsaveoptions}

Renders the shape into an SVG image and saves into a stream.


```python
def save(self, stream: io.BytesIO, save_options: aspose.words.saving.SvgSaveOptions):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| stream | io.BytesIO | The stream where to save the SVG image of the shape. |
| save_options | [SvgSaveOptions](../../../aspose.words.saving/svgsaveoptions/) | Specifies the options that control how the shape is rendered and saved. Can be ``None``. If this is ``None``, the image will be saved with the default options. |

## Examples

Shows how to render an Office Math object into an image file in the local file system.

```python
doc = aw.Document(MY_DIR + 'Office math.docx')
math = doc.get_child(aw.NodeType.OFFICE_MATH, 0, True).as_office_math()
# Create an "ImageSaveOptions" object to pass to the node renderer's "save" method to modify
# how it renders the OfficeMath node into an image.
save_options = aw.saving.ImageSaveOptions(aw.SaveFormat.PNG)
# Set the "scale" property to 5 to render the object to five times its original size.
save_options.scale = 5
math.get_math_renderer().save(ARTIFACTS_DIR + 'Shape.render_office_math.png', save_options)
```

Shows how to pass save options when rendering office math.

```python
doc = aw.Document(file_name=MY_DIR + 'Office math.docx')
math = doc.get_child(aw.NodeType.OFFICE_MATH, 0, True).as_office_math()
options = aw.saving.SvgSaveOptions()
options.text_output_mode = aw.saving.SvgTextOutputMode.USE_PLACED_GLYPHS
math.get_math_renderer().save(file_name=ARTIFACTS_DIR + 'SvgSaveOptions.Output.svg', save_options=options)
```

Shows how to use a shape renderer to export shapes to files in the local file system.

```python
doc = aw.Document(file_name=MY_DIR + 'Various shapes.docx')
shapes = [x.as_shape() for x in list(doc.get_child_nodes(aw.NodeType.SHAPE, True)) if isinstance(x.as_shape(), aw.drawing.Shape)]
self.assertEqual(7, len(shapes))
# There are 7 shapes in the document, including one group shape with 2 child shapes.
# We will render every shape to an image file in the local file system
# while ignoring the group shapes since they have no appearance.
# This will produce 6 image files.
for shape in [x.as_shape() for x in list(doc.get_child_nodes(aw.NodeType.SHAPE, True)) if isinstance(x.as_shape(), aw.drawing.Shape)]:
    renderer = shape.get_shape_renderer()
    options = aw.saving.ImageSaveOptions(aw.SaveFormat.PNG)
    renderer.save(file_name=ARTIFACTS_DIR + f'Shape.RenderAllShapes.{shape.name}.png', save_options=options)
```

## See Also

* module [aspose.words.rendering](../../)
* class [NodeRendererBase](../)

