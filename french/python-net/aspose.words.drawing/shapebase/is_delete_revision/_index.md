---
title: ShapeBase.is_delete_revision property
linktitle: is_delete_revision property
articleTitle: is_delete_revision property
second_title: Aspose.Words for Python
description: "ShapeBase.is_delete_revision property. Returns true if this object was deleted in Microsoft Word while change tracking was enabled."
type: docs
weight: 270
url: /fr/python-net/aspose.words.drawing/shapebase/is_delete_revision/
---

## ShapeBase.is_delete_revision property

Returns true if this object was deleted in Microsoft Word while change tracking was enabled.


```python
@property
def is_delete_revision(self) -> bool:
    ...

```

### Examples

Shows how to work with revision shapes.

```python
doc = aw.Document()
self.assertFalse(doc.track_revisions)
# Insérez une forme en ligne sans suivi des révisions, ce qui fera que cette forme ne sera pas une révision de quelque nature que ce soit.
shape = aw.drawing.Shape(doc, aw.drawing.ShapeType.CUBE)
shape.wrap_type = aw.drawing.WrapType.INLINE
shape.width = 100
shape.height = 100
doc.first_section.body.first_paragraph.append_child(shape)
# Commencez le suivi des révisions puis insérez une autre forme, qui sera une révision.
doc.start_track_revisions(author='John Doe')
shape = aw.drawing.Shape(doc, aw.drawing.ShapeType.SUN)
shape.wrap_type = aw.drawing.WrapType.INLINE
shape.width = 100
shape.height = 100
doc.first_section.body.first_paragraph.append_child(shape)
shapes = list(filter(lambda a: a is not None, map(lambda b: system_helper.linq.Enumerable.of_type(lambda x: x.as_shape(), b), list(doc.get_child_nodes(aw.NodeType.SHAPE, True)))))
self.assertEqual(2, len(shapes))
shapes[0].remove()
# Puisque nous avons supprimé cette forme pendant que nous suivions les modifications,
# la forme persiste dans le document et compte comme une révision de suppression.
# Accepter cette révision supprimera la forme de façon permanente, et la rejeter la conservera dans le document.
self.assertEqual(aw.drawing.ShapeType.CUBE, shapes[0].shape_type)
self.assertTrue(shapes[0].is_delete_revision)
# Et nous avons inséré une autre forme pendant le suivi des modifications, de sorte que cette forme comptera comme une révision d'insertion.
# Accepter cette révision assimilera cette forme au document en tant que non‑révision,
# et rejeter la révision supprimera cette forme de façon permanente.
self.assertEqual(aw.drawing.ShapeType.SUN, shapes[1].shape_type)
self.assertTrue(shapes[1].is_insert_revision)
```

### See Also

* module [aspose.words.drawing](../../)
* class [ShapeBase](../)

