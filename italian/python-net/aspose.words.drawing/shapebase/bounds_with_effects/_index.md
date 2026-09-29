---
title: ShapeBase.bounds_with_effects property
linktitle: bounds_with_effects property
articleTitle: bounds_with_effects property
second_title: Aspose.Words for Python
description: "ShapeBase.bounds_with_effects property. Gets final extent that this shape object has after applying drawing effects"
type: docs
weight: 90
url: /it/python-net/aspose.words.drawing/shapebase/bounds_with_effects/
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
# Le due forme sono identiche in termini di dimensioni e tipo di forma.
self.assertEqual(shapes[0].width, shapes[1].width)
self.assertEqual(shapes[0].height, shapes[1].height)
self.assertEqual(shapes[0].shape_type, shapes[1].shape_type)
# La prima forma non ha effetti, mentre la seconda ha un'ombra e un contorno spesso.
# Questi effetti rendono la silhouette della seconda forma più grande di quella della prima.
# Anche se le dimensioni del rettangolo compaiono quando facciamo clic su queste forme in Microsoft Word,
# i confini esterni visibili della seconda forma sono influenzati dall'ombra e dal contorno e quindi sono più grandi.
# Possiamo usare il metodo "AdjustWithEffects" per vedere la dimensione reale della forma.
self.assertEqual(0, shapes[0].stroke_weight)
self.assertEqual(20, shapes[1].stroke_weight)
self.assertFalse(shapes[0].shadow_enabled)
self.assertTrue(shapes[1].shadow_enabled)
shape = shapes[0]
# Crea un oggetto RectangleF, che rappresenta un rettangolo,
# che potremmo potenzialmente usare come coordinate e limiti per una forma.
rectangle_f = aspose.pydrawing.RectangleF(200, 200, 1000, 1000)
# Esegui questo metodo per ottenere le dimensioni del rettangolo aggiustate per tutti i nostri effetti di forma.
rectangle_f_out = shape.adjust_with_effects(rectangle_f)
# Poiché la forma non ha effetti che modificano il bordo, le sue dimensioni di contorno non sono influenzate.
self.assertEqual(200, rectangle_f_out.x)
self.assertEqual(200, rectangle_f_out.y)
self.assertEqual(1000, rectangle_f_out.width)
self.assertEqual(1000, rectangle_f_out.height)
# Verifica l'estensione finale della prima forma, in punti.
self.assertEqual(0, shape.bounds_with_effects.x)
self.assertEqual(0, shape.bounds_with_effects.y)
self.assertEqual(147, shape.bounds_with_effects.width)
self.assertEqual(147, shape.bounds_with_effects.height)
shape = shapes[1]
rectangle_f = aspose.pydrawing.RectangleF(200, 200, 1000, 1000)
rectangle_f_out = shape.adjust_with_effects(rectangle_f)
# Gli effetti della forma hanno spostato leggermente l'angolo superiore sinistro apparente della forma.
self.assertEqual(171.5, rectangle_f_out.x)
self.assertEqual(167, rectangle_f_out.y)
# Gli effetti hanno anche influenzato le dimensioni visibili della forma.
self.assertEqual(1045, rectangle_f_out.width)
self.assertEqual(1133.5, rectangle_f_out.height)
# Gli effetti hanno anche influenzato i limiti visibili della forma.
self.assertEqual(-28.5, shape.bounds_with_effects.x)
self.assertEqual(-33, shape.bounds_with_effects.y)
self.assertEqual(192, shape.bounds_with_effects.width)
self.assertEqual(280.5, shape.bounds_with_effects.height)
```

### See Also

* module [aspose.words.drawing](../../)
* class [ShapeBase](../)

