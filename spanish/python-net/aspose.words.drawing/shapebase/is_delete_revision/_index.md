---
title: ShapeBase.is_delete_revision property
linktitle: is_delete_revision property
articleTitle: is_delete_revision property
second_title: Aspose.Words for Python
description: "ShapeBase.is_delete_revision property. Returns true if this object was deleted in Microsoft Word while change tracking was enabled."
type: docs
weight: 270
url: /es/python-net/aspose.words.drawing/shapebase/is_delete_revision/
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
# Inserte una forma incrustada sin rastrear revisiones, lo que hará que esta forma no sea una revisión de ningún tipo.
shape = aw.drawing.Shape(doc, aw.drawing.ShapeType.CUBE)
shape.wrap_type = aw.drawing.WrapType.INLINE
shape.width = 100
shape.height = 100
doc.first_section.body.first_paragraph.append_child(shape)
# Comience a rastrear revisiones y luego inserte otra forma, lo que será una revisión.
doc.start_track_revisions(author='John Doe')
shape = aw.drawing.Shape(doc, aw.drawing.ShapeType.SUN)
shape.wrap_type = aw.drawing.WrapType.INLINE
shape.width = 100
shape.height = 100
doc.first_section.body.first_paragraph.append_child(shape)
shapes = list(filter(lambda a: a is not None, map(lambda b: system_helper.linq.Enumerable.of_type(lambda x: x.as_shape(), b), list(doc.get_child_nodes(aw.NodeType.SHAPE, True)))))
self.assertEqual(2, len(shapes))
shapes[0].remove()
# Dado que eliminamos esa forma mientras rastreábamos cambios,
# la forma persiste en el documento y cuenta como una revisión de eliminación.
# Aceptar esta revisión eliminará la forma permanentemente, y rechazarla la mantendrá en el documento.
self.assertEqual(aw.drawing.ShapeType.CUBE, shapes[0].shape_type)
self.assertTrue(shapes[0].is_delete_revision)
# Y insertamos otra forma mientras rastreábamos cambios, por lo que esa forma contará como una revisión de inserción.
# Aceptar esta revisión asimilará esta forma al documento como una no-revisión,
# y rechazar la revisión eliminará esta forma permanentemente.
self.assertEqual(aw.drawing.ShapeType.SUN, shapes[1].shape_type)
self.assertTrue(shapes[1].is_insert_revision)
```

### See Also

* module [aspose.words.drawing](../../)
* class [ShapeBase](../)

