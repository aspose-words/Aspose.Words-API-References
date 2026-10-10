---
title: ShapeBase.adjust_with_effects method
linktitle: adjust_with_effects method
articleTitle: adjust_with_effects method
second_title: Aspose.Words for Python
description: "ShapeBase.adjust_with_effects method. Adds to the source rectangle values of the effect extent and returns the final rectangle."
type: docs
weight: 660
url: /tr/python-net/aspose.words.drawing/shapebase/adjust_with_effects/
---

## adjust_with_effects(source) {#rectanglef}

Adds to the source rectangle values of the effect extent and returns the final rectangle.


```python
def adjust_with_effects(self, source: aspose.pydrawing.RectangleF):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| source | aspose.pydrawing.RectangleF |  |

### Examples

Shows how to check how a shape's bounds are affected by shape effects.

```python
doc = aw.Document(file_name=MY_DIR + 'Shape shadow effect.docx')
shapes = list(filter(lambda a: a is not None, map(lambda b: system_helper.linq.Enumerable.of_type(lambda x: x.as_shape(), b), list(doc.get_child_nodes(aw.NodeType.SHAPE, True)))))
self.assertEqual(2, len(shapes))
# İki şekil, boyutlar ve şekil türü açısından özdeştir.
self.assertEqual(shapes[0].width, shapes[1].width)
self.assertEqual(shapes[0].height, shapes[1].height)
self.assertEqual(shapes[0].shape_type, shapes[1].shape_type)
# İlk şeklin hiçbir etkisi yoktur, ikinci şeklin ise bir gölgesi ve kalın bir kenarlığı vardır.
# Bu etkiler, ikinci şeklin siluet boyutunu birincisinininkinden daha büyük yapar.
# Microsoft Word'de bu şekillere tıkladığımızda dikdörtgenin boyutu görünsede,
# ikinci şeklin görünen dış sınırları gölge ve kenarlık tarafından etkilenir ve bu yüzden daha büyüktür.
# Şeklin gerçek boyutunu görmek için "AdjustWithEffects" metodunu kullanabiliriz.
self.assertEqual(0, shapes[0].stroke_weight)
self.assertEqual(20, shapes[1].stroke_weight)
self.assertFalse(shapes[0].shadow_enabled)
self.assertTrue(shapes[1].shadow_enabled)
shape = shapes[0]
# Bir dikdörtgeni temsil eden RectangleF nesnesi oluşturun,
# bu nesneyi potansiyel olarak bir şeklin koordinatları ve sınırları olarak kullanabiliriz.
rectangle_f = aspose.pydrawing.RectangleF(200, 200, 1000, 1000)
# Bu metodu çalıştırarak dikdörtgenin, şekil etkilerimize göre ayarlanmış boyutunu elde edin.
rectangle_f_out = shape.adjust_with_effects(rectangle_f)
# Şeklin kenar değiştiren bir etkisi olmadığından, sınır boyutları etkilenmez.
self.assertEqual(200, rectangle_f_out.x)
self.assertEqual(200, rectangle_f_out.y)
self.assertEqual(1000, rectangle_f_out.width)
self.assertEqual(1000, rectangle_f_out.height)
# İlk şeklin son kapsamını, puan cinsinden doğrulayın.
self.assertEqual(0, shape.bounds_with_effects.x)
self.assertEqual(0, shape.bounds_with_effects.y)
self.assertEqual(147, shape.bounds_with_effects.width)
self.assertEqual(147, shape.bounds_with_effects.height)
shape = shapes[1]
rectangle_f = aspose.pydrawing.RectangleF(200, 200, 1000, 1000)
rectangle_f_out = shape.adjust_with_effects(rectangle_f)
# Şekil etkileri, şeklin görünen sol üst köşesini hafifçe kaydırdı.
self.assertEqual(171.5, rectangle_f_out.x)
self.assertEqual(167, rectangle_f_out.y)
# Etkiler ayrıca şeklin görünen boyutlarını etkiledi.
self.assertEqual(1045, rectangle_f_out.width)
self.assertEqual(1133.5, rectangle_f_out.height)
# Etkiler ayrıca şeklin görünen sınırlarını etkiledi.
self.assertEqual(-28.5, shape.bounds_with_effects.x)
self.assertEqual(-33, shape.bounds_with_effects.y)
self.assertEqual(192, shape.bounds_with_effects.width)
self.assertEqual(280.5, shape.bounds_with_effects.height)
```

### See Also

* module [aspose.words.drawing](../../)
* class [ShapeBase](../)

