---
title: ShapeBase.soft_edge property
linktitle: soft_edge property
articleTitle: soft_edge property
second_title: Aspose.Words for Python
description: "ShapeBase.soft_edge property. Gets soft edge formatting for the shape."
type: docs
weight: 550
url: /it/python-net/aspose.words.drawing/shapebase/soft_edge/
---

## ShapeBase.soft_edge property

Gets soft edge formatting for the shape.


```python
@property
def soft_edge(self) -> aspose.words.drawing.SoftEdgeFormat:
    ...

```

### Examples

Shows how to work with soft edge formatting.

```python
builder = aw.DocumentBuilder()
shape = builder.insert_shape(shape_type=aw.drawing.ShapeType.RECTANGLE, width=200, height=200)
# Applica un bordo morbido alla forma.
shape.soft_edge.radius = 30
builder.document.save(file_name=ARTIFACTS_DIR + 'Shape.SoftEdge.docx')
# Carica il documento con una forma rettangolare con bordo morbido.
doc = aw.Document(file_name=ARTIFACTS_DIR + 'Shape.SoftEdge.docx')
shape = doc.get_child(aw.NodeType.SHAPE, 0, True).as_shape()
soft_edge_format = shape.soft_edge
# Verifica il raggio del bordo morbido.
self.assertEqual(30, soft_edge_format.radius)
# Rimuovi il bordo morbido dalla forma.
soft_edge_format.remove()
# Verifica il raggio del bordo morbido rimosso.
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
* class [ShapeBase](../)

