---
title: ShapeBase.bounds_with_effects property
linktitle: bounds_with_effects property
articleTitle: bounds_with_effects property
second_title: Aspose.Words for Python
description: "ShapeBase.bounds_with_effects property. Gets final extent that this shape object has after applying drawing effects"
type: docs
weight: 90
url: /zh/python-net/aspose.words.drawing/shapebase/bounds_with_effects/
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
# 这两个形状在尺寸和形状类型方面是相同的。
self.assertEqual(shapes[0].width, shapes[1].width)
self.assertEqual(shapes[0].height, shapes[1].height)
self.assertEqual(shapes[0].shape_type, shapes[1].shape_type)
# 第一个形状没有任何效果，而第二个形状有阴影和粗轮廓。
# 这些效果使第二个形状的轮廓尺寸大于第一个形状的尺寸。
# 即使在 Microsoft Word 中单击这些形状时矩形的大小会显示出来，
# 第二个形状的可见外部边界受到阴影和轮廓的影响，因此更大。
# 我们可以使用 "AdjustWithEffects" 方法来查看形状的真实大小。
self.assertEqual(0, shapes[0].stroke_weight)
self.assertEqual(20, shapes[1].stroke_weight)
self.assertFalse(shapes[0].shadow_enabled)
self.assertTrue(shapes[1].shadow_enabled)
shape = shapes[0]
# 创建一个 RectangleF 对象，表示一个矩形，
# 我们可以将其用作形状的坐标和边界。
rectangle_f = aspose.pydrawing.RectangleF(200, 200, 1000, 1000)
# 运行此方法以获取考虑所有形状效果后矩形的大小。
rectangle_f_out = shape.adjust_with_effects(rectangle_f)
# 由于该形状没有改变边框的效果，其边界尺寸不受影响。
self.assertEqual(200, rectangle_f_out.x)
self.assertEqual(200, rectangle_f_out.y)
self.assertEqual(1000, rectangle_f_out.width)
self.assertEqual(1000, rectangle_f_out.height)
# 验证第一个形状的最终范围（以点为单位）。
self.assertEqual(0, shape.bounds_with_effects.x)
self.assertEqual(0, shape.bounds_with_effects.y)
self.assertEqual(147, shape.bounds_with_effects.width)
self.assertEqual(147, shape.bounds_with_effects.height)
shape = shapes[1]
rectangle_f = aspose.pydrawing.RectangleF(200, 200, 1000, 1000)
rectangle_f_out = shape.adjust_with_effects(rectangle_f)
# 形状效果略微移动了形状的左上角位置。
self.assertEqual(171.5, rectangle_f_out.x)
self.assertEqual(167, rectangle_f_out.y)
# 这些效果也影响了形状的可见尺寸。
self.assertEqual(1045, rectangle_f_out.width)
self.assertEqual(1133.5, rectangle_f_out.height)
# 这些效果也影响了形状的可见边界。
self.assertEqual(-28.5, shape.bounds_with_effects.x)
self.assertEqual(-33, shape.bounds_with_effects.y)
self.assertEqual(192, shape.bounds_with_effects.width)
self.assertEqual(280.5, shape.bounds_with_effects.height)
```

### See Also

* module [aspose.words.drawing](../../)
* class [ShapeBase](../)

