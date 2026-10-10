---
title: ShapeBase.is_delete_revision property
linktitle: is_delete_revision property
articleTitle: is_delete_revision property
second_title: Aspose.Words for Python
description: "ShapeBase.is_delete_revision property. Returns true if this object was deleted in Microsoft Word while change tracking was enabled."
type: docs
weight: 270
url: /de/python-net/aspose.words.drawing/shapebase/is_delete_revision/
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
# Fügen Sie eine Inline-Form ohne Verfolgung von Änderungen ein, wodurch diese Form keine Revision irgendeiner Art darstellt.
shape = aw.drawing.Shape(doc, aw.drawing.ShapeType.CUBE)
shape.wrap_type = aw.drawing.WrapType.INLINE
shape.width = 100
shape.height = 100
doc.first_section.body.first_paragraph.append_child(shape)
# Beginnen Sie die Verfolgung von Änderungen und fügen Sie dann eine weitere Form ein, die eine Revision sein wird.
doc.start_track_revisions(author='John Doe')
shape = aw.drawing.Shape(doc, aw.drawing.ShapeType.SUN)
shape.wrap_type = aw.drawing.WrapType.INLINE
shape.width = 100
shape.height = 100
doc.first_section.body.first_paragraph.append_child(shape)
shapes = list(filter(lambda a: a is not None, map(lambda b: system_helper.linq.Enumerable.of_type(lambda x: x.as_shape(), b), list(doc.get_child_nodes(aw.NodeType.SHAPE, True)))))
self.assertEqual(2, len(shapes))
shapes[0].remove()
# Da wir diese Form entfernt haben, während wir Änderungen verfolgt haben,
# bleibt die Form im Dokument erhalten und zählt als Löschrevision.
# Das Akzeptieren dieser Revision entfernt die Form dauerhaft, und das Ablehnen lässt sie im Dokument erhalten.
self.assertEqual(aw.drawing.ShapeType.CUBE, shapes[0].shape_type)
self.assertTrue(shapes[0].is_delete_revision)
# Und wir haben eine weitere Form eingefügt, während Änderungen verfolgt wurden, sodass diese Form als Einfüge‑Revision gezählt wird.
# Das Akzeptieren dieser Revision wird diese Form in das Dokument als Nicht-Revision einbinden,
# und das Ablehnen der Revision wird diese Form dauerhaft entfernen.
self.assertEqual(aw.drawing.ShapeType.SUN, shapes[1].shape_type)
self.assertTrue(shapes[1].is_insert_revision)
```

### See Also

* module [aspose.words.drawing](../../)
* class [ShapeBase](../)

