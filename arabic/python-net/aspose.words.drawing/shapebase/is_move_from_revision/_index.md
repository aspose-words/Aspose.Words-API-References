---
title: ShapeBase.is_move_from_revision property
linktitle: is_move_from_revision property
articleTitle: is_move_from_revision property
second_title: Aspose.Words for Python
description: "ShapeBase.is_move_from_revision property. Returns ``True`` if this object was moved (deleted) in Microsoft Word while change tracking was enabled."
type: docs
weight: 340
url: /ar/python-net/aspose.words.drawing/shapebase/is_move_from_revision/
---

## ShapeBase.is_move_from_revision property

Returns ``True`` if this object was moved (deleted) in Microsoft Word while change tracking was enabled.



```python
@property
def is_move_from_revision(self) -> bool:
    ...

```

### Examples

Shows how to identify move revision shapes.

```python
# مراجعة النقل هي عندما نقوم بنقل عنصر في جسم المستند عن طريق القص واللصق في Microsoft Word أثناء
# تتبع التغييرات. إذا شاركنا شكلاً مضمنًا في مثل هذا النقل النصي، فإن ذلك الشكل سيكون أيضًا مراجعة.
# النسخ واللصق أو نقل الأشكال العائمة لا يخلق مراجعات نقل.
doc = aw.Document(file_name=MY_DIR + 'Revision shape.docx')
# تتكون مراجعات النقل من أزواج من مراجعات "Move from" و "Move to". لقد نقلنا في هذا المستند شكلًا واحدًا،
# ولكن حتى نقبل أو نرفض مراجعة النقل، سيبقى هناك نسختان من ذلك الشكل.
shapes = list(filter(lambda a: a is not None, map(lambda b: system_helper.linq.Enumerable.of_type(lambda x: x.as_shape(), b), list(doc.get_child_nodes(aw.NodeType.SHAPE, True)))))
self.assertEqual(2, len(shapes))
# This هو تعديل "Move to"، وهو الشكل في وجهة وصوله.
# إذا قبلنا التعديل، سيختفي شكل تعديل "Move to" هذا،
# وسيظل شكل تعديل "Move from" موجودًا.
self.assertFalse(shapes[0].is_move_from_revision)
self.assertTrue(shapes[0].is_move_to_revision)
# هذا هو تعديل "Move from"، وهو الشكل في موقعه الأصلي.
# إذا قبلنا التعديل، سيختفي شكل تعديل "Move from" هذا،
# وسيظل شكل تعديل "Move to" موجودًا.
self.assertTrue(shapes[1].is_move_from_revision)
self.assertFalse(shapes[1].is_move_to_revision)
```

### See Also

* module [aspose.words.drawing](../../)
* class [ShapeBase](../)

