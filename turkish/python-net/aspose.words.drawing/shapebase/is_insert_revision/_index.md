---
title: ShapeBase.is_insert_revision property
linktitle: is_insert_revision property
articleTitle: is_insert_revision property
second_title: Aspose.Words for Python
description: "ShapeBase.is_insert_revision property. Returns true if this object was inserted in Microsoft Word while change tracking was enabled."
type: docs
weight: 320
url: /tr/python-net/aspose.words.drawing/shapebase/is_insert_revision/
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
# Revizyonları izlemeksizin satır içi bir şekil ekleyin, bu da şeklin herhangi bir revizyon olmamasını sağlar.
shape = aw.drawing.Shape(doc, aw.drawing.ShapeType.CUBE)
shape.wrap_type = aw.drawing.WrapType.INLINE
shape.width = 100
shape.height = 100
doc.first_section.body.first_paragraph.append_child(shape)
# Revizyon izlemeyi başlatın ve ardından başka bir şekil ekleyin, bu bir revizyon olacaktır.
doc.start_track_revisions(author='John Doe')
shape = aw.drawing.Shape(doc, aw.drawing.ShapeType.SUN)
shape.wrap_type = aw.drawing.WrapType.INLINE
shape.width = 100
shape.height = 100
doc.first_section.body.first_paragraph.append_child(shape)
shapes = list(filter(lambda a: a is not None, map(lambda b: system_helper.linq.Enumerable.of_type(lambda x: x.as_shape(), b), list(doc.get_child_nodes(aw.NodeType.SHAPE, True)))))
self.assertEqual(2, len(shapes))
shapes[0].remove()
# Değişiklikleri izlerken o şekli kaldırdığımız için,
# şekil belgede kalır ve bir silme revizyonu olarak sayılır.
# Bu revizyonu kabul etmek şekli kalıcı olarak kaldırır, reddetmek ise belgede tutar.
self.assertEqual(aw.drawing.ShapeType.CUBE, shapes[0].shape_type)
self.assertTrue(shapes[0].is_delete_revision)
# Ve değişiklikleri izlerken başka bir şekil ekledik, bu yüzden o şekil bir ekleme revizyonu olarak sayılacak.
# Bu revizyonu kabul etmek, bu şekli belgeye revizyon olmayan bir öğe olarak asimile eder,
# ve revizyonu reddetmek bu şekli kalıcı olarak kaldıracaktır.
self.assertEqual(aw.drawing.ShapeType.SUN, shapes[1].shape_type)
self.assertTrue(shapes[1].is_insert_revision)
```

### See Also

* module [aspose.words.drawing](../../)
* class [ShapeBase](../)

