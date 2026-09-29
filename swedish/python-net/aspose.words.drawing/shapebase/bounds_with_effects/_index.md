---
title: ShapeBase.bounds_with_effects property
linktitle: bounds_with_effects property
articleTitle: bounds_with_effects property
second_title: Aspose.Words for Python
description: "ShapeBase.bounds_with_effects property. Gets final extent that this shape object has after applying drawing effects"
type: docs
weight: 90
url: /sv/python-net/aspose.words.drawing/shapebase/bounds_with_effects/
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
# De två formerna är identiska när det gäller dimensioner och formtyp.
self.assertEqual(shapes[0].width, shapes[1].width)
self.assertEqual(shapes[0].height, shapes[1].height)
self.assertEqual(shapes[0].shape_type, shapes[1].shape_type)
# Den första formen har inga effekter, och den andra har en skugga och en tjock kontur.
# Dessa effekter gör siluettens storlek på den andra formen större än den första.
# Även om rektangelns storlek visas när vi klickar på dessa former i Microsoft Word,
# så påverkas de synliga yttre gränserna för den andra formen av skuggan och konturen och är därför större.
# Vi kan använda metoden "AdjustWithEffects" för att se den verkliga storleken på formen.
self.assertEqual(0, shapes[0].stroke_weight)
self.assertEqual(20, shapes[1].stroke_weight)
self.assertFalse(shapes[0].shadow_enabled)
self.assertTrue(shapes[1].shadow_enabled)
shape = shapes[0]
# Skapa ett RectangleF-objekt som representerar en rektangel,
# som vi potentiellt kan använda som koordinater och gränser för en form.
rectangle_f = aspose.pydrawing.RectangleF(200, 200, 1000, 1000)
# Kör den här metoden för att få rektangelns storlek justerad för alla våra formeffekter.
rectangle_f_out = shape.adjust_with_effects(rectangle_f)
# Eftersom formen inte har några kantförändrande effekter, är dess gränsdimensioner opåverkade.
self.assertEqual(200, rectangle_f_out.x)
self.assertEqual(200, rectangle_f_out.y)
self.assertEqual(1000, rectangle_f_out.width)
self.assertEqual(1000, rectangle_f_out.height)
# Verifiera den slutgiltiga omfattningen av den första formen, i punkter.
self.assertEqual(0, shape.bounds_with_effects.x)
self.assertEqual(0, shape.bounds_with_effects.y)
self.assertEqual(147, shape.bounds_with_effects.width)
self.assertEqual(147, shape.bounds_with_effects.height)
shape = shapes[1]
rectangle_f = aspose.pydrawing.RectangleF(200, 200, 1000, 1000)
rectangle_f_out = shape.adjust_with_effects(rectangle_f)
# Formeffekterna har flyttat det synliga övre vänstra hörnet av formen något.
self.assertEqual(171.5, rectangle_f_out.x)
self.assertEqual(167, rectangle_f_out.y)
# Effekterna har också påverkat formens synliga dimensioner.
self.assertEqual(1045, rectangle_f_out.width)
self.assertEqual(1133.5, rectangle_f_out.height)
# Effekterna har också påverkat formens synliga gränser.
self.assertEqual(-28.5, shape.bounds_with_effects.x)
self.assertEqual(-33, shape.bounds_with_effects.y)
self.assertEqual(192, shape.bounds_with_effects.width)
self.assertEqual(280.5, shape.bounds_with_effects.height)
```

### See Also

* module [aspose.words.drawing](../../)
* class [ShapeBase](../)

