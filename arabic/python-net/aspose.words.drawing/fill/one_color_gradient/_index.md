---
title: Fill.one_color_gradient method
linktitle: one_color_gradient method
articleTitle: one_color_gradient method
second_title: Aspose.Words for Python
description: "aspose.words.drawing.Fill.one_color_gradient method"
type: docs
weight: 220
url: /ar/python-net/aspose.words.drawing/fill/one_color_gradient/
---

## one_color_gradient(style, variant, degree) {#gradientstyle_gradientvariant_float}

Sets the specified fill to a one-color gradient.


```python
def one_color_gradient(self, style: aspose.words.drawing.GradientStyle, variant: aspose.words.drawing.GradientVariant, degree: float):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| style | [GradientStyle](../../gradientstyle/) | The gradient style [GradientStyle](../../gradientstyle/) |
| variant | [GradientVariant](../../gradientvariant/) | The gradient variant [GradientVariant](../../gradientvariant/) |
| degree | float | The gradient degree. Can be a value from 0.0 (dark) to 1.0 (light). |

## one_color_gradient(color, style, variant, degree) {#color_gradientstyle_gradientvariant_float}

Sets the specified fill to a one-color gradient using the specified color.


```python
def one_color_gradient(self, color: aspose.pydrawing.Color, style: aspose.words.drawing.GradientStyle, variant: aspose.words.drawing.GradientVariant, degree: float):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| color | aspose.pydrawing.Color | The color to build the gradient. |
| style | [GradientStyle](../../gradientstyle/) | The gradient style [GradientStyle](../../gradientstyle/) |
| variant | [GradientVariant](../../gradientvariant/) | The gradient variant [GradientVariant](../../gradientvariant/) |
| degree | float | The gradient degree. Can be a value from 0.0 (dark) to 1.0 (light). |

## Examples

Shows how to fill a shape with a gradients.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
shape = builder.insert_shape(shape_type=aw.drawing.ShapeType.RECTANGLE, width=80, height=80)
# طبق تعبئة تدرج لون أحادي على الشكل بلون ForeColor لتدرج التعبئة.
shape.fill.one_color_gradient(color=aspose.pydrawing.Color.red, style=aw.drawing.GradientStyle.HORIZONTAL, variant=aw.drawing.GradientVariant.VARIANT2, degree=0.1)
self.assertEqual(aspose.pydrawing.Color.red.to_argb(), shape.fill.fore_color.to_argb())
self.assertEqual(aw.drawing.GradientStyle.HORIZONTAL, shape.fill.gradient_style)
self.assertEqual(aw.drawing.GradientVariant.VARIANT2, shape.fill.gradient_variant)
self.assertEqual(270, shape.fill.gradient_angle)
shape = builder.insert_shape(shape_type=aw.drawing.ShapeType.RECTANGLE, width=80, height=80)
# تطبيق تعبئة تدرج لوني ثنائي اللون على الشكل.
shape.fill.two_color_gradient(style=aw.drawing.GradientStyle.FROM_CORNER, variant=aw.drawing.GradientVariant.VARIANT4)
# تغيير BackColor لتعبئة التدرج.
shape.fill.back_color = aspose.pydrawing.Color.yellow
# لاحظ أن التغييرات في "GradientAngle" لـ "GradientStyle.FromCorner/GradientStyle.FromCenter"
# تعبئة التدرج لا تُحدث أي تأثير، ستعمل فقط مع التدرج الخطي.
shape.fill.gradient_angle = 15
self.assertEqual(aspose.pydrawing.Color.yellow.to_argb(), shape.fill.back_color.to_argb())
self.assertEqual(aw.drawing.GradientStyle.FROM_CORNER, shape.fill.gradient_style)
self.assertEqual(aw.drawing.GradientVariant.VARIANT4, shape.fill.gradient_variant)
self.assertEqual(0, shape.fill.gradient_angle)
# استخدم خيار الامتثال لتعريف الشكل باستخدام DML إذا كنت تريد الحصول على "GradientStyle",
# "GradientVariant" و "GradientAngle" خصائص بعد حفظ المستند.
save_options = aw.saving.OoxmlSaveOptions()
save_options.compliance = aw.saving.OoxmlCompliance.ISO29500_2008_STRICT
doc.save(file_name=ARTIFACTS_DIR + 'Shape.GradientFill.docx', save_options=save_options)
```

## See Also

* module [aspose.words.drawing](../../)
* class [Fill](../)

