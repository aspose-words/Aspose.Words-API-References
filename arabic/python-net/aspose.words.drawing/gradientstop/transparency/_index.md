---
title: GradientStop.transparency property
linktitle: transparency property
articleTitle: transparency property
second_title: Aspose.Words for Python
description: "GradientStop.transparency property. Gets or sets a value representing the transparency of the gradient fill expressed as a percent in range 0.0 to 1.0."
type: docs
weight: 50
url: /ar/python-net/aspose.words.drawing/gradientstop/transparency/
---

## GradientStop.transparency property

Gets or sets a value representing the transparency of the gradient fill
expressed as a percent in range 0.0 to 1.0.


```python
@property
def transparency(self) -> float:
    ...

@transparency.setter
def transparency(self, value: float):
    ...

```

### Examples

Shows how to add gradient stops to the gradient fill.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
shape = builder.insert_shape(shape_type=aw.drawing.ShapeType.RECTANGLE, width=80, height=80)
shape.fill.two_color_gradient(color1=aspose.pydrawing.Color.green, color2=aspose.pydrawing.Color.red, style=aw.drawing.GradientStyle.HORIZONTAL, variant=aw.drawing.GradientVariant.VARIANT2)
# احصل على مجموعة نقاط التدرج.
gradient_stops = shape.fill.gradient_stops
# غيّر أول نقطة تدرج.
gradient_stops[0].color = aspose.pydrawing.Color.aqua
gradient_stops[0].position = 0.1
gradient_stops[0].transparency = 0.25
# أضف نقطة تدرج جديدة إلى نهاية المجموعة.
gradient_stop = aw.drawing.GradientStop(color=aspose.pydrawing.Color.brown, position=0.5)
gradient_stops.add(gradient_stop)
# أزل نقطة التدرج عند الفهرس 1.
gradient_stops.remove_at(1)
# وأدرج نقطة تدرج جديدة عند نفس الفهرس 1.
gradient_stops.insert(1, aw.drawing.GradientStop(color=aspose.pydrawing.Color.chocolate, position=0.75, transparency=0.3))
# إزالة آخر نقطة تدرج في المجموعة.
gradient_stop = gradient_stops[2]
gradient_stops.remove(gradient_stop)
self.assertEqual(2, gradient_stops.count)
self.assertEqual(aspose.pydrawing.Color.from_argb(255, 0, 255, 255), gradient_stops[0].base_color)
self.assertEqual(aspose.pydrawing.Color.aqua.to_argb(), gradient_stops[0].color.to_argb())
self.assertAlmostEqual(0.1, gradient_stops[0].position, delta=0.01)
self.assertAlmostEqual(0.25, gradient_stops[0].transparency, delta=0.01)
self.assertEqual(aspose.pydrawing.Color.chocolate.to_argb(), gradient_stops[1].color.to_argb())
self.assertAlmostEqual(0.75, gradient_stops[1].position, delta=0.01)
self.assertAlmostEqual(0.3, gradient_stops[1].transparency, delta=0.01)
# استخدم خيار الامتثال لتحديد الشكل باستخدام DML
# إذا كنت تريد الحصول على الخاصية "GradientStops" بعد حفظ المستند.
save_options = aw.saving.OoxmlSaveOptions()
save_options.compliance = aw.saving.OoxmlCompliance.ISO29500_2008_STRICT
doc.save(file_name=ARTIFACTS_DIR + 'Shape.GradientStops.docx', save_options=save_options)
```

### See Also

* module [aspose.words.drawing](../../)
* class [GradientStop](../)

