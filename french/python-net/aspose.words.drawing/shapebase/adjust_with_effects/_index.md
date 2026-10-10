---
title: ShapeBase.adjust_with_effects method
linktitle: adjust_with_effects method
articleTitle: adjust_with_effects method
second_title: Aspose.Words for Python
description: "ShapeBase.adjust_with_effects method. Adds to the source rectangle values of the effect extent and returns the final rectangle."
type: docs
weight: 660
url: /fr/python-net/aspose.words.drawing/shapebase/adjust_with_effects/
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
# Les deux formes sont identiques en termes de dimensions et de type de forme.
self.assertEqual(shapes[0].width, shapes[1].width)
self.assertEqual(shapes[0].height, shapes[1].height)
self.assertEqual(shapes[0].shape_type, shapes[1].shape_type)
# La première forme n’a aucun effet, et la seconde possède une ombre et un contour épais.
# Ces effets rendent la taille de la silhouette de la seconde forme plus grande que celle de la première.
# Même si la taille du rectangle apparaît lorsque nous cliquons sur ces formes dans Microsoft Word,
# les limites extérieures visibles de la seconde forme sont affectées par l’ombre et le contour et sont donc plus grandes.
# Nous pouvons utiliser la méthode "AdjustWithEffects" pour voir la vraie taille de la forme.
self.assertEqual(0, shapes[0].stroke_weight)
self.assertEqual(20, shapes[1].stroke_weight)
self.assertFalse(shapes[0].shadow_enabled)
self.assertTrue(shapes[1].shadow_enabled)
shape = shapes[0]
# Créez un objet RectangleF, représentant un rectangle,
# que nous pourrions éventuellement utiliser comme coordonnées et limites pour une forme.
rectangle_f = aspose.pydrawing.RectangleF(200, 200, 1000, 1000)
# Exécutez cette méthode pour obtenir la taille du rectangle ajustée à tous nos effets de forme.
rectangle_f_out = shape.adjust_with_effects(rectangle_f)
# Comme la forme n’a aucun effet modifiant la bordure, ses dimensions de frontière ne sont pas affectées.
self.assertEqual(200, rectangle_f_out.x)
self.assertEqual(200, rectangle_f_out.y)
self.assertEqual(1000, rectangle_f_out.width)
self.assertEqual(1000, rectangle_f_out.height)
# Vérifiez l’étendue finale de la première forme, en points.
self.assertEqual(0, shape.bounds_with_effects.x)
self.assertEqual(0, shape.bounds_with_effects.y)
self.assertEqual(147, shape.bounds_with_effects.width)
self.assertEqual(147, shape.bounds_with_effects.height)
shape = shapes[1]
rectangle_f = aspose.pydrawing.RectangleF(200, 200, 1000, 1000)
rectangle_f_out = shape.adjust_with_effects(rectangle_f)
# Les effets de forme ont déplacé légèrement le coin supérieur gauche apparent de la forme.
self.assertEqual(171.5, rectangle_f_out.x)
self.assertEqual(167, rectangle_f_out.y)
# Les effets ont également affecté les dimensions visibles de la forme.
self.assertEqual(1045, rectangle_f_out.width)
self.assertEqual(1133.5, rectangle_f_out.height)
# Les effets ont également affecté les limites visibles de la forme.
self.assertEqual(-28.5, shape.bounds_with_effects.x)
self.assertEqual(-33, shape.bounds_with_effects.y)
self.assertEqual(192, shape.bounds_with_effects.width)
self.assertEqual(280.5, shape.bounds_with_effects.height)
```

### See Also

* module [aspose.words.drawing](../../)
* class [ShapeBase](../)

