---
title: ShapeBase.is_move_to_revision property
linktitle: is_move_to_revision property
articleTitle: is_move_to_revision property
second_title: Aspose.Words for Python
description: "ShapeBase.is_move_to_revision property. Returns ``True`` if this object was moved (inserted) in Microsoft Word while change tracking was enabled."
type: docs
weight: 340
url: /python-net/aspose.words.drawing/shapebase/is_move_to_revision/
---

## ShapeBase.is_move_to_revision property

Returns ``True`` if this object was moved (inserted) in Microsoft Word while change tracking was enabled.



```python
@property
def is_move_to_revision(self) -> bool:
    ...

```

### Examples

Shows how to identify move revision shapes.

```python
# A move revision is when we move an element in the document body by cut-and-pasting it in Microsoft Word while
# tracking changes. If we involve an inline shape in such a text movement, that shape will also be a revision.
# Copying-and-pasting or moving floating shapes do not create move revisions.
doc = aw.Document(MY_DIR + 'Revision shape.docx')
# Move revisions consist of pairs of "Move from", and "Move to" revisions. We moved in this document in one shape,
# but until we accept or reject the move revision, there will be two instances of that shape.
shapes = [node.as_shape() for node in doc.get_child_nodes(aw.NodeType.SHAPE, True)]
self.assertEqual(2, len(shapes))
# This is the "Move to" revision, which is the shape at its arrival destination.
# If we accept the revision, this "Move to" revision shape will disappear,
# and the "Move from" revision shape will remain.
self.assertFalse(shapes[0].is_move_from_revision)
self.assertTrue(shapes[0].is_move_to_revision)
# This is the "Move from" revision, which is the shape at its original location.
# If we accept the revision, this "Move from" revision shape will disappear,
# and the "Move to" revision shape will remain.
self.assertTrue(shapes[1].is_move_from_revision)
self.assertFalse(shapes[1].is_move_to_revision)
```

### See Also

* module [aspose.words.drawing](../../)
* class [ShapeBase](../)

