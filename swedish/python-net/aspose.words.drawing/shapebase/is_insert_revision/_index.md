---
title: ShapeBase.is_insert_revision property
linktitle: is_insert_revision property
articleTitle: is_insert_revision property
second_title: Aspose.Words for Python
description: "ShapeBase.is_insert_revision property. Returns true if this object was inserted in Microsoft Word while change tracking was enabled."
type: docs
weight: 320
url: /sv/python-net/aspose.words.drawing/shapebase/is_insert_revision/
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
# Infoga en inline-form utan att spåra revideringar, vilket gör att denna form inte blir någon revidering alls.
shape = aw.drawing.Shape(doc, aw.drawing.ShapeType.CUBE)
shape.wrap_type = aw.drawing.WrapType.INLINE
shape.width = 100
shape.height = 100
doc.first_section.body.first_paragraph.append_child(shape)
# Börja spåra revideringar och infoga sedan en annan form, vilket blir en revidering.
doc.start_track_revisions(author='John Doe')
shape = aw.drawing.Shape(doc, aw.drawing.ShapeType.SUN)
shape.wrap_type = aw.drawing.WrapType.INLINE
shape.width = 100
shape.height = 100
doc.first_section.body.first_paragraph.append_child(shape)
shapes = list(filter(lambda a: a is not None, map(lambda b: system_helper.linq.Enumerable.of_type(lambda x: x.as_shape(), b), list(doc.get_child_nodes(aw.NodeType.SHAPE, True)))))
self.assertEqual(2, len(shapes))
shapes[0].remove()
# Eftersom vi tog bort den formen medan vi spårade ändringar,
# fortsätter formen att finnas i dokumentet och räknas som en raderingsrevidering.
# Att acceptera denna revidering kommer att ta bort formen permanent, och att avvisa den kommer att behålla den i dokumentet.
self.assertEqual(aw.drawing.ShapeType.CUBE, shapes[0].shape_type)
self.assertTrue(shapes[0].is_delete_revision)
# Och vi infogade en annan form medan vi spårade ändringar, så den formen kommer att räknas som en insättningsrevidering.
# Att acceptera den här revisionen kommer att assimilera den här formen till dokumentet som en icke-revision,
# och att avvisa revisionen kommer att ta bort den här formen permanent.
self.assertEqual(aw.drawing.ShapeType.SUN, shapes[1].shape_type)
self.assertTrue(shapes[1].is_insert_revision)
```

### See Also

* module [aspose.words.drawing](../../)
* class [ShapeBase](../)

