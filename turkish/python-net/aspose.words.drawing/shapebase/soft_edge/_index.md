---
title: ShapeBase.soft_edge property
linktitle: soft_edge property
articleTitle: soft_edge property
second_title: Aspose.Words for Python
description: "ShapeBase.soft_edge property. Gets soft edge formatting for the shape."
type: docs
weight: 550
url: /tr/python-net/aspose.words.drawing/shapebase/soft_edge/
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
# Şekle yumuşak kenar uygula.
shape.soft_edge.radius = 30
builder.document.save(file_name=ARTIFACTS_DIR + 'Shape.SoftEdge.docx')
# Yumuşak kenarlı dikdörtgen şekilli belgeyi yükle.
doc = aw.Document(file_name=ARTIFACTS_DIR + 'Shape.SoftEdge.docx')
shape = doc.get_child(aw.NodeType.SHAPE, 0, True).as_shape()
soft_edge_format = shape.soft_edge
# Yumuşak kenar yarıçapını kontrol et.
self.assertEqual(30, soft_edge_format.radius)
# Şekilden yumuşak kenarı kaldır.
soft_edge_format.remove()
# Kaldırılan yumuşak kenarın yarıçapını kontrol et.
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

