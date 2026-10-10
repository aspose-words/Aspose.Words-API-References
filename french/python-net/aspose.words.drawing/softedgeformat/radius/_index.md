---
title: SoftEdgeFormat.radius property
linktitle: radius property
articleTitle: radius property
second_title: Aspose.Words for Python
description: "SoftEdgeFormat.radius property. Gets or sets a double value that represents the length of the radius for a soft edge effect in points (pt)"
type: docs
weight: 10
url: /fr/python-net/aspose.words.drawing/softedgeformat/radius/
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
# Appliquer un bord doux à la forme.
shape.soft_edge.radius = 30
builder.document.save(file_name=ARTIFACTS_DIR + 'Shape.SoftEdge.docx')
# Charger le document avec une forme rectangulaire à bord doux.
doc = aw.Document(file_name=ARTIFACTS_DIR + 'Shape.SoftEdge.docx')
shape = doc.get_child(aw.NodeType.SHAPE, 0, True).as_shape()
soft_edge_format = shape.soft_edge
# Vérifier le rayon du bord doux.
self.assertEqual(30, soft_edge_format.radius)
# Supprimer le bord doux de la forme.
soft_edge_format.remove()
# Vérifier le rayon du bord doux supprimé.
self.assertEqual(0, soft_edge_format.radius)
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

