---
title: ShapeBase.bounds_with_effects property
linktitle: bounds_with_effects property
articleTitle: bounds_with_effects property
second_title: Aspose.Words for Python
description: "ShapeBase.bounds_with_effects property. Gets final extent that this shape object has after applying drawing effects"
type: docs
weight: 90
url: /de/python-net/aspose.words.drawing/shapebase/bounds_with_effects/
---

## ShapeBase.bounds_with_effects property

Gets final extent that this shape object has after applying drawing effects.
Value is measured in points.


```python
@property
def bounds_with_effects(self) -> aspose.pydrawing.RectangleF:
    ...

```

### Examples

Shows how to check how a shape's bounds are affected by shape effects.

```python
doc = aw.Document(file_name=MY_DIR + 'Shape shadow effect.docx')
shapes = list(filter(lambda a: a is not None, map(lambda b: system_helper.linq.Enumerable.of_type(lambda x: x.as_shape(), b), list(doc.get_child_nodes(aw.NodeType.SHAPE, True)))))
self.assertEqual(2, len(shapes))
# Die beiden Formen sind hinsichtlich Abmessungen und Formtyp identisch.
self.assertEqual(shapes[0].width, shapes[1].width)
self.assertEqual(shapes[0].height, shapes[1].height)
self.assertEqual(shapes[0].shape_type, shapes[1].shape_type)
# Die erste Form hat keine Effekte, und die zweite hat einen Schatten und eine dicke Kontur.
# Diese Effekte vergrößern die Silhouette der zweiten Form im Vergleich zur ersten.
# Auch wenn die Größe des Rechtecks angezeigt wird, wenn wir in Microsoft Word auf diese Formen klicken,
# sind die sichtbaren äußeren Begrenzungen der zweiten Form durch den Schatten und die Kontur beeinflusst und daher größer.
# Wir können die Methode "AdjustWithEffects" verwenden, um die wahre Größe der Form zu sehen.
self.assertEqual(0, shapes[0].stroke_weight)
self.assertEqual(20, shapes[1].stroke_weight)
self.assertFalse(shapes[0].shadow_enabled)
self.assertTrue(shapes[1].shadow_enabled)
shape = shapes[0]
# Erstellen Sie ein RectangleF-Objekt, das ein Rechteck darstellt,
# das wir potenziell als Koordinaten und Begrenzungen für eine Form verwenden könnten.
rectangle_f = aspose.pydrawing.RectangleF(200, 200, 1000, 1000)
# Führen Sie diese Methode aus, um die Größe des Rechtecks zu erhalten, die für alle unsere Formeffekte angepasst ist.
rectangle_f_out = shape.adjust_with_effects(rectangle_f)
# Da die Form keine randverändernden Effekte hat, bleiben ihre Begrenzungsabmessungen unverändert.
self.assertEqual(200, rectangle_f_out.x)
self.assertEqual(200, rectangle_f_out.y)
self.assertEqual(1000, rectangle_f_out.width)
self.assertEqual(1000, rectangle_f_out.height)
# Überprüfen Sie die endgültige Ausdehnung der ersten Form in Punkten.
self.assertEqual(0, shape.bounds_with_effects.x)
self.assertEqual(0, shape.bounds_with_effects.y)
self.assertEqual(147, shape.bounds_with_effects.width)
self.assertEqual(147, shape.bounds_with_effects.height)
shape = shapes[1]
rectangle_f = aspose.pydrawing.RectangleF(200, 200, 1000, 1000)
rectangle_f_out = shape.adjust_with_effects(rectangle_f)
# Die Formeffekte haben die scheinbare obere linke Ecke der Form leicht verschoben.
self.assertEqual(171.5, rectangle_f_out.x)
self.assertEqual(167, rectangle_f_out.y)
# Die Effekte haben zudem die sichtbaren Abmessungen der Form beeinflusst.
self.assertEqual(1045, rectangle_f_out.width)
self.assertEqual(1133.5, rectangle_f_out.height)
# Die Effekte haben zudem die sichtbaren Begrenzungen der Form beeinflusst.
self.assertEqual(-28.5, shape.bounds_with_effects.x)
self.assertEqual(-33, shape.bounds_with_effects.y)
self.assertEqual(192, shape.bounds_with_effects.width)
self.assertEqual(280.5, shape.bounds_with_effects.height)
```

### See Also

* module [aspose.words.drawing](../../)
* class [ShapeBase](../)

