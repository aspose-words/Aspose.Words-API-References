---
title: ShapeBase.is_insert_revision property
linktitle: is_insert_revision property
articleTitle: is_insert_revision property
second_title: Aspose.Words for Python
description: "ShapeBase.is_insert_revision property. Returns true if this object was inserted in Microsoft Word while change tracking was enabled."
type: docs
weight: 320
url: /ar/python-net/aspose.words.drawing/shapebase/is_insert_revision/
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
# أدرج شكلاً مضمنًا دون تتبع التعديلات، مما سيجعل هذا الشكل ليس تعديلًا من أي نوع.
shape = aw.drawing.Shape(doc, aw.drawing.ShapeType.CUBE)
shape.wrap_type = aw.drawing.WrapType.INLINE
shape.width = 100
shape.height = 100
doc.first_section.body.first_paragraph.append_child(shape)
# ابدأ تتبع التعديلات ثم أدخل شكلًا آخر، سيكون تعديلًا.
doc.start_track_revisions(author='John Doe')
shape = aw.drawing.Shape(doc, aw.drawing.ShapeType.SUN)
shape.wrap_type = aw.drawing.WrapType.INLINE
shape.width = 100
shape.height = 100
doc.first_section.body.first_paragraph.append_child(shape)
shapes = list(filter(lambda a: a is not None, map(lambda b: system_helper.linq.Enumerable.of_type(lambda x: x.as_shape(), b), list(doc.get_child_nodes(aw.NodeType.SHAPE, True)))))
self.assertEqual(2, len(shapes))
shapes[0].remove()
# نظرًا لأننا أزلنا ذلك الشكل أثناء تتبع التغييرات،
# يبقى الشكل في المستند ويُحسب كتعديل حذف.
# قبول هذا التعديل سيزيل الشكل نهائيًا، ورفضه سيبقيه في المستند.
self.assertEqual(aw.drawing.ShapeType.CUBE, shapes[0].shape_type)
self.assertTrue(shapes[0].is_delete_revision)
# وقد أدخلنا شكلًا آخر أثناء تتبع التغييرات، لذا سيُحسب ذلك الشكل كتعديل إدراج.
# قبول هذا التعديل سيُدمج هذا الشكل في المستند كغير تعديل،
# ورفض التعديل سيزيل هذا الشكل بشكل دائم.
self.assertEqual(aw.drawing.ShapeType.SUN, shapes[1].shape_type)
self.assertTrue(shapes[1].is_insert_revision)
```

### See Also

* module [aspose.words.drawing](../../)
* class [ShapeBase](../)

