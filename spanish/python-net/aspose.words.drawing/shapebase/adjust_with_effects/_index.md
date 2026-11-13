---
title: ShapeBase.adjust_with_effects method
linktitle: adjust_with_effects method
articleTitle: adjust_with_effects method
second_title: Aspose.Words for Python
description: "ShapeBase.adjust_with_effects method. Adds to the source rectangle values of the effect extent and returns the final rectangle."
type: docs
weight: 660
url: /es/python-net/aspose.words.drawing/shapebase/adjust_with_effects/
---

## adjust_with_effects(source) {#rectanglef}

Adds to the source rectangle values of the effect extent and returns the final rectangle.


```python
def adjust_with_effects(self, source: aspose.pydrawing.RectangleF):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| source | aspose.pydrawing.RectangleF |  |

### Examples

Shows how to check how a shape's bounds are affected by shape effects.

```python
doc = aw.Document(file_name=MY_DIR + 'Shape shadow effect.docx')
shapes = list(filter(lambda a: a is not None, map(lambda b: system_helper.linq.Enumerable.of_type(lambda x: x.as_shape(), b), list(doc.get_child_nodes(aw.NodeType.SHAPE, True)))))
self.assertEqual(2, len(shapes))
# Las dos formas son idénticas en cuanto a dimensiones y tipo de forma.
self.assertEqual(shapes[0].width, shapes[1].width)
self.assertEqual(shapes[0].height, shapes[1].height)
self.assertEqual(shapes[0].shape_type, shapes[1].shape_type)
# La primera forma no tiene efectos, y la segunda tiene una sombra y un contorno grueso.
# Estos efectos hacen que el tamaño de la silueta de la segunda forma sea mayor que el de la primera.
# Aunque el tamaño del rectángulo aparece cuando hacemos clic en estas formas en Microsoft Word,
# los límites exteriores visibles de la segunda forma están afectados por la sombra y el contorno y, por lo tanto, son mayores.
# Podemos usar el método "AdjustWithEffects" para ver el tamaño real de la forma.
self.assertEqual(0, shapes[0].stroke_weight)
self.assertEqual(20, shapes[1].stroke_weight)
self.assertFalse(shapes[0].shadow_enabled)
self.assertTrue(shapes[1].shadow_enabled)
shape = shapes[0]
# Cree un objeto RectangleF, que representa un rectángulo,
# que podríamos usar potencialmente como las coordenadas y los límites de una forma.
rectangle_f = aspose.pydrawing.RectangleF(200, 200, 1000, 1000)
# Ejecute este método para obtener el tamaño del rectángulo ajustado a todos nuestros efectos de forma.
rectangle_f_out = shape.adjust_with_effects(rectangle_f)
# Dado que la forma no tiene efectos que cambien el borde, sus dimensiones de límite no se ven afectadas.
self.assertEqual(200, rectangle_f_out.x)
self.assertEqual(200, rectangle_f_out.y)
self.assertEqual(1000, rectangle_f_out.width)
self.assertEqual(1000, rectangle_f_out.height)
# Verifique la extensión final de la primera forma, en puntos.
self.assertEqual(0, shape.bounds_with_effects.x)
self.assertEqual(0, shape.bounds_with_effects.y)
self.assertEqual(147, shape.bounds_with_effects.width)
self.assertEqual(147, shape.bounds_with_effects.height)
shape = shapes[1]
rectangle_f = aspose.pydrawing.RectangleF(200, 200, 1000, 1000)
rectangle_f_out = shape.adjust_with_effects(rectangle_f)
# Los efectos de la forma han desplazado ligeramente la esquina superior izquierda aparente de la forma.
self.assertEqual(171.5, rectangle_f_out.x)
self.assertEqual(167, rectangle_f_out.y)
# Los efectos también han afectado las dimensiones visibles de la forma.
self.assertEqual(1045, rectangle_f_out.width)
self.assertEqual(1133.5, rectangle_f_out.height)
# Los efectos también han afectado los límites visibles de la forma.
self.assertEqual(-28.5, shape.bounds_with_effects.x)
self.assertEqual(-33, shape.bounds_with_effects.y)
self.assertEqual(192, shape.bounds_with_effects.width)
self.assertEqual(280.5, shape.bounds_with_effects.height)
```

### See Also

* module [aspose.words.drawing](../../)
* class [ShapeBase](../)

