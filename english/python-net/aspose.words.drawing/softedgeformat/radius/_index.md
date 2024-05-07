---
title: SoftEdgeFormat.radius property
linktitle: radius property
articleTitle: radius property
second_title: Aspose.Words for Python
description: "SoftEdgeFormat.radius property. Gets or sets a double value that represents the length of the radius for a soft edge effect in points (pt)"
type: docs
weight: 10
url: /python-net/aspose.words.drawing/softedgeformat/radius/
---

## SoftEdgeFormat.radius property

Gets or sets a double value that represents the length of the radius for a soft edge effect in points (pt).
The default value is 0.0.


```python
@property
def radius(self) -> float:
    ...

@radius.setter
def radius(self, value: float):
    ...

```

### Examples

Shows how to work with soft edge formatting.

```python
builder = aw.DocumentBuilder()
shape = builder.insert_shape(shape_type=aw.drawing.ShapeType.RECTANGLE, width=200, height=200)
# Apply soft edge to the shape.
shape.soft_edge.radius = 30
builder.document.save(file_name=ARTIFACTS_DIR + 'Shape.SoftEdge.docx')
# Load document with rectangle shape with soft edge.
doc = aw.Document(file_name=ARTIFACTS_DIR + 'Shape.SoftEdge.docx')
shape = doc.get_child(aw.NodeType.SHAPE, 0, True).as_shape()
# Check soft edge radius.
self.assertEqual(30, shape.soft_edge.radius)
# Remove soft edge from the shape.
shape.soft_edge.remove()
# Check radius of the removed soft edge.
self.assertEqual(0, shape.soft_edge.radius)
```

Shows how to set limit for image resolution.

```python
doc = aw.Document(file_name=MY_DIR + 'Rendering.docx')
save_options = aw.saving.SvgSaveOptions()
save_options.max_image_resolution = 72
doc.save(file_name=ARTIFACTS_DIR + 'SvgSaveOptions.MaxImageResolution.svg', save_options=save_options)
```

### See Also

* module [aspose.words.drawing](../../)
* class [SoftEdgeFormat](../)

