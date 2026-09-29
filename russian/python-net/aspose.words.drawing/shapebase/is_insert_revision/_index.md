---
title: ShapeBase.is_insert_revision property
linktitle: is_insert_revision property
articleTitle: is_insert_revision property
second_title: Aspose.Words for Python
description: "ShapeBase.is_insert_revision property. Returns true if this object was inserted in Microsoft Word while change tracking was enabled."
type: docs
weight: 320
url: /ru/python-net/aspose.words.drawing/shapebase/is_insert_revision/
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
# Вставьте встроенную фигуру без отслеживания изменений, что сделает эту фигуру не являющейся изменением любого типа.
shape = aw.drawing.Shape(doc, aw.drawing.ShapeType.CUBE)
shape.wrap_type = aw.drawing.WrapType.INLINE
shape.width = 100
shape.height = 100
doc.first_section.body.first_paragraph.append_child(shape)
# Начните отслеживание изменений, а затем вставьте другую фигуру, которая будет изменением.
doc.start_track_revisions(author='John Doe')
shape = aw.drawing.Shape(doc, aw.drawing.ShapeType.SUN)
shape.wrap_type = aw.drawing.WrapType.INLINE
shape.width = 100
shape.height = 100
doc.first_section.body.first_paragraph.append_child(shape)
shapes = list(filter(lambda a: a is not None, map(lambda b: system_helper.linq.Enumerable.of_type(lambda x: x.as_shape(), b), list(doc.get_child_nodes(aw.NodeType.SHAPE, True)))))
self.assertEqual(2, len(shapes))
shapes[0].remove()
# Поскольку мы удалили эту фигуру, пока отслеживали изменения,
# фигура остаётся в документе и считается удалением.
# Принятие этого изменения удалит фигуру навсегда, а отклонение оставит её в документе.
self.assertEqual(aw.drawing.ShapeType.CUBE, shapes[0].shape_type)
self.assertTrue(shapes[0].is_delete_revision)
# И мы вставили другую фигуру во время отслеживания изменений, поэтому эта фигура будет считаться вставкой.
# Принятие этой правки включит эту форму в документ как неправку,
# а отклонение правки навсегда удалит эту форму.
self.assertEqual(aw.drawing.ShapeType.SUN, shapes[1].shape_type)
self.assertTrue(shapes[1].is_insert_revision)
```

### See Also

* module [aspose.words.drawing](../../)
* class [ShapeBase](../)

