---
title: ShapeBase.is_insert_revision property
linktitle: is_insert_revision property
articleTitle: is_insert_revision property
second_title: Aspose.Words for Python
description: "ShapeBase.is_insert_revision property. Returns true if this object was inserted in Microsoft Word while change tracking was enabled."
type: docs
weight: 310
url: /python-net/aspose.words.drawing/shapebase/is_insert_revision/
---

## ShapeBase.is_insert_revision property

Returns true if this object was inserted in Microsoft Word while change tracking was enabled.


```python
@property
def is_insert_revision(self) -> bool:
    ...

```

### Examples

Shows how to work with revision shapes.

```python
doc = aw.Document()

self.assertFalse(doc.track_revisions)

# Insert an inline shape without tracking revisions, which will make this shape not a revision of any kind.
shape = aw.drawing.Shape(doc, aw.drawing.ShapeType.CUBE)
shape.wrap_type = aw.drawing.WrapType.INLINE
shape.width = 100.0
shape.height = 100.0
doc.first_section.body.first_paragraph.append_child(shape)

# Start tracking revisions and then insert another shape, which will be a revision.
doc.start_track_revisions("John Doe")

shape = aw.drawing.Shape(doc, aw.drawing.ShapeType.SUN)
shape.wrap_type = aw.drawing.WrapType.INLINE
shape.width = 100.0
shape.height = 100.0
doc.first_section.body.first_paragraph.append_child(shape)

shapes = [node.as_shape() for node in doc.get_child_nodes(aw.NodeType.SHAPE, True)]

self.assertEqual(2, len(shapes))

shapes[0].remove()

# Since we removed that shape while we were tracking changes,
# the shape persists in the document and counts as a delete revision.
# Accepting this revision will remove the shape permanently, and rejecting it will keep it in the document.
self.assertEqual(aw.drawing.ShapeType.CUBE, shapes[0].shape_type)
self.assertTrue(shapes[0].is_delete_revision)

# And we inserted another shape while tracking changes, so that shape will count as an insert revision.
# Accepting this revision will assimilate this shape into the document as a non-revision,
# and rejecting the revision will remove this shape permanently.
self.assertEqual(aw.drawing.ShapeType.SUN, shapes[1].shape_type)
self.assertTrue(shapes[1].is_insert_revision)
```

### See Also

* module [aspose.words.drawing](../../)
* class [ShapeBase](../)

