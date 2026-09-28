---
title: ShapeBase.bounds_with_effects property
linktitle: bounds_with_effects property
articleTitle: bounds_with_effects property
second_title: Aspose.Words for Python
description: "ShapeBase.bounds_with_effects property. Gets final extent that this shape object has after applying drawing effects"
type: docs
weight: 90
url: /ar/python-net/aspose.words.drawing/shapebase/bounds_with_effects/
---

## ShapeBase.bounds_with_effects property

Gets final extent that this shape object has after applying drawing effects.
Value is measured in points.


```python
@property
def bounds_with_effects(self) -> aspose.pydrawing.RectangleF:
    ...

```

### Examples

Shows how to check how a shape's bounds are affected by shape effects.

```python
doc = aw.Document(file_name=MY_DIR + 'Shape shadow effect.docx')
shapes = list(filter(lambda a: a is not None, map(lambda b: system_helper.linq.Enumerable.of_type(lambda x: x.as_shape(), b), list(doc.get_child_nodes(aw.NodeType.SHAPE, True)))))
self.assertEqual(2, len(shapes))
# الشكلان متطابقان من حيث الأبعاد ونوع الشكل.
self.assertEqual(shapes[0].width, shapes[1].width)
self.assertEqual(shapes[0].height, shapes[1].height)
self.assertEqual(shapes[0].shape_type, shapes[1].shape_type)
# الشكل الأول لا يحتوي على تأثيرات، والثاني لديه ظل وحدود سميكة.
# هذه التأثيرات تجعل حجم ظل الشكل الثاني أكبر من حجم الشكل الأول.
# حتى وإن ظهر حجم المستطيل عندما نضغط على هذه الأشكال في Microsoft Word،
# الحدود الخارجية المرئية للشكل الثاني تتأثر بالظل والحدود وبالتالي تكون أكبر.
# يمكننا استخدام طريقة "AdjustWithEffects" لرؤية الحجم الحقيقي للشكل.
self.assertEqual(0, shapes[0].stroke_weight)
self.assertEqual(20, shapes[1].stroke_weight)
self.assertFalse(shapes[0].shadow_enabled)
self.assertTrue(shapes[1].shadow_enabled)
shape = shapes[0]
# إنشاء كائن RectangleF، يمثل مستطيلًا،
# والذي يمكننا احتماليًا استخدامه كإحداثيات وحدود لشكل.
rectangle_f = aspose.pydrawing.RectangleF(200, 200, 1000, 1000)
# تشغيل هذه الطريقة للحصول على حجم المستطيل المعدل لجميع تأثيرات الشكل لدينا.
rectangle_f_out = shape.adjust_with_effects(rectangle_f)
# نظرًا لأن الشكل لا يحتوي على تأثيرات تغير الحدود، فإن أبعاد حدوده لا تتأثر.
self.assertEqual(200, rectangle_f_out.x)
self.assertEqual(200, rectangle_f_out.y)
self.assertEqual(1000, rectangle_f_out.width)
self.assertEqual(1000, rectangle_f_out.height)
# تحقق من الامتداد النهائي للشكل الأول، بالنقاط.
self.assertEqual(0, shape.bounds_with_effects.x)
self.assertEqual(0, shape.bounds_with_effects.y)
self.assertEqual(147, shape.bounds_with_effects.width)
self.assertEqual(147, shape.bounds_with_effects.height)
shape = shapes[1]
rectangle_f = aspose.pydrawing.RectangleF(200, 200, 1000, 1000)
rectangle_f_out = shape.adjust_with_effects(rectangle_f)
# تأثيرات الشكل قد حركت الزاوية العليا اليسرى الظاهرة للشكل قليلاً.
self.assertEqual(171.5, rectangle_f_out.x)
self.assertEqual(167, rectangle_f_out.y)
# التأثيرات أثرت أيضًا على الأبعاد المرئية للشكل.
self.assertEqual(1045, rectangle_f_out.width)
self.assertEqual(1133.5, rectangle_f_out.height)
# التأثيرات أثرت أيضًا على الحدود المرئية للشكل.
self.assertEqual(-28.5, shape.bounds_with_effects.x)
self.assertEqual(-33, shape.bounds_with_effects.y)
self.assertEqual(192, shape.bounds_with_effects.width)
self.assertEqual(280.5, shape.bounds_with_effects.height)
```

### See Also

* module [aspose.words.drawing](../../)
* class [ShapeBase](../)

