---
title: ShapeBase.bounds_with_effects property
linktitle: bounds_with_effects property
articleTitle: bounds_with_effects property
second_title: Aspose.Words for Python
description: "ShapeBase.bounds_with_effects property. Gets final extent that this shape object has after applying drawing effects"
type: docs
weight: 90
url: /ru/python-net/aspose.words.drawing/shapebase/bounds_with_effects/
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
# Две формы идентичны по размерам и типу формы.
self.assertEqual(shapes[0].width, shapes[1].width)
self.assertEqual(shapes[0].height, shapes[1].height)
self.assertEqual(shapes[0].shape_type, shapes[1].shape_type)
# У первой формы нет эффектов, а у второй есть тень и толстая обводка.
# Эти эффекты делают размер силуэта второй формы больше, чем у первой.
# Хотя размер прямоугольника отображается, когда мы щёлкаем по этим формам в Microsoft Word,
# видимые внешние границы второй формы изменяются тенью и обводкой и поэтому становятся больше.
# Мы можем использовать метод "AdjustWithEffects", чтобы увидеть истинный размер формы.
self.assertEqual(0, shapes[0].stroke_weight)
self.assertEqual(20, shapes[1].stroke_weight)
self.assertFalse(shapes[0].shadow_enabled)
self.assertTrue(shapes[1].shadow_enabled)
shape = shapes[0]
# Создайте объект RectangleF, представляющий прямоугольник,
# который мы потенциально можем использовать в качестве координат и границ для формы.
rectangle_f = aspose.pydrawing.RectangleF(200, 200, 1000, 1000)
# Выполните этот метод, чтобы получить размер прямоугольника, скорректированный со всеми нашими эффектами формы.
rectangle_f_out = shape.adjust_with_effects(rectangle_f)
# Поскольку у формы нет эффектов, меняющих границу, её размеры границы остаются неизменными.
self.assertEqual(200, rectangle_f_out.x)
self.assertEqual(200, rectangle_f_out.y)
self.assertEqual(1000, rectangle_f_out.width)
self.assertEqual(1000, rectangle_f_out.height)
# Проверьте окончательный размер первой формы в пунктах.
self.assertEqual(0, shape.bounds_with_effects.x)
self.assertEqual(0, shape.bounds_with_effects.y)
self.assertEqual(147, shape.bounds_with_effects.width)
self.assertEqual(147, shape.bounds_with_effects.height)
shape = shapes[1]
rectangle_f = aspose.pydrawing.RectangleF(200, 200, 1000, 1000)
rectangle_f_out = shape.adjust_with_effects(rectangle_f)
# Эффекты формы слегка сместили видимый верхний левый угол формы.
self.assertEqual(171.5, rectangle_f_out.x)
self.assertEqual(167, rectangle_f_out.y)
# Эффекты также повлияли на видимые размеры формы.
self.assertEqual(1045, rectangle_f_out.width)
self.assertEqual(1133.5, rectangle_f_out.height)
# Эффекты также повлияли на видимые границы формы.
self.assertEqual(-28.5, shape.bounds_with_effects.x)
self.assertEqual(-33, shape.bounds_with_effects.y)
self.assertEqual(192, shape.bounds_with_effects.width)
self.assertEqual(280.5, shape.bounds_with_effects.height)
```

### See Also

* module [aspose.words.drawing](../../)
* class [ShapeBase](../)

