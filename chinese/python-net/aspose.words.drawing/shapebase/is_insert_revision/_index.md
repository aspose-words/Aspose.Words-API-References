---
title: ShapeBase.is_insert_revision property
linktitle: is_insert_revision property
articleTitle: is_insert_revision property
second_title: Aspose.Words for Python
description: "ShapeBase.is_insert_revision property. Returns true if this object was inserted in Microsoft Word while change tracking was enabled."
type: docs
weight: 320
url: /zh/python-net/aspose.words.drawing/shapebase/is_insert_revision/
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
# 插入一个不跟踪修订的内联形状，这将使该形状不成为任何类型的修订。
shape = aw.drawing.Shape(doc, aw.drawing.ShapeType.CUBE)
shape.wrap_type = aw.drawing.WrapType.INLINE
shape.width = 100
shape.height = 100
doc.first_section.body.first_paragraph.append_child(shape)
# 开始跟踪修订，然后插入另一个形状，该形状将成为一次修订。
doc.start_track_revisions(author='John Doe')
shape = aw.drawing.Shape(doc, aw.drawing.ShapeType.SUN)
shape.wrap_type = aw.drawing.WrapType.INLINE
shape.width = 100
shape.height = 100
doc.first_section.body.first_paragraph.append_child(shape)
shapes = list(filter(lambda a: a is not None, map(lambda b: system_helper.linq.Enumerable.of_type(lambda x: x.as_shape(), b), list(doc.get_child_nodes(aw.NodeType.SHAPE, True)))))
self.assertEqual(2, len(shapes))
shapes[0].remove()
# 由于我们在跟踪更改时删除了该形状，
# 该形状仍然保留在文档中，并计为删除修订。
# 接受此修订将永久删除该形状，拒绝则会保留在文档中。
self.assertEqual(aw.drawing.ShapeType.CUBE, shapes[0].shape_type)
self.assertTrue(shapes[0].is_delete_revision)
# 并且我们在跟踪更改时插入了另一个形状，因此该形状将计为插入修订。
# 接受此修订将把此形状合并到文档中，作为非修订，
# 并且拒绝此修订将永久删除此形状。
self.assertEqual(aw.drawing.ShapeType.SUN, shapes[1].shape_type)
self.assertTrue(shapes[1].is_insert_revision)
```

### See Also

* module [aspose.words.drawing](../../)
* class [ShapeBase](../)

