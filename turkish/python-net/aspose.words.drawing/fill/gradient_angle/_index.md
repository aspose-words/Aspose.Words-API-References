---
title: Fill.gradient_angle property
linktitle: gradient_angle property
articleTitle: gradient_angle property
second_title: Aspose.Words for Python
description: "Fill.gradient_angle property. Gets or sets the angle of the gradient fill."
type: docs
weight: 100
url: /tr/python-net/aspose.words.drawing/fill/gradient_angle/
---

## Fill.gradient_angle property

Gets or sets the angle of the gradient fill.


```python
@property
def gradient_angle(self) -> float:
    ...

@gradient_angle.setter
def gradient_angle(self, value: float):
    ...

```

### Examples

Shows how to fill a shape with a gradients.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
shape = builder.insert_shape(shape_type=aw.drawing.ShapeType.RECTANGLE, width=80, height=80)
# Şekle, degrade doldurmanın ÖnRengi ile Tek renkli degrade doldurma uygula.
shape.fill.one_color_gradient(color=aspose.pydrawing.Color.red, style=aw.drawing.GradientStyle.HORIZONTAL, variant=aw.drawing.GradientVariant.VARIANT2, degree=0.1)
self.assertEqual(aspose.pydrawing.Color.red.to_argb(), shape.fill.fore_color.to_argb())
self.assertEqual(aw.drawing.GradientStyle.HORIZONTAL, shape.fill.gradient_style)
self.assertEqual(aw.drawing.GradientVariant.VARIANT2, shape.fill.gradient_variant)
self.assertEqual(270, shape.fill.gradient_angle)
shape = builder.insert_shape(shape_type=aw.drawing.ShapeType.RECTANGLE, width=80, height=80)
# Şekle iki renkli degrade doldurma uygula.
shape.fill.two_color_gradient(style=aw.drawing.GradientStyle.FROM_CORNER, variant=aw.drawing.GradientVariant.VARIANT4)
# Degrade doldurmanın BackColor değerini değiştir.
shape.fill.back_color = aspose.pydrawing.Color.yellow
# Şunu not edin: \"GradientAngle\" değişiklikleri \"GradientStyle.FromCorner/GradientStyle.FromCenter\" için.
# degrade doldurma hiçbir etki göstermez, yalnızca doğrusal degrade için çalışır.
shape.fill.gradient_angle = 15
self.assertEqual(aspose.pydrawing.Color.yellow.to_argb(), shape.fill.back_color.to_argb())
self.assertEqual(aw.drawing.GradientStyle.FROM_CORNER, shape.fill.gradient_style)
self.assertEqual(aw.drawing.GradientVariant.VARIANT4, shape.fill.gradient_variant)
self.assertEqual(0, shape.fill.gradient_angle)
# Şekli DML kullanarak tanımlamak için uyumluluk seçeneğini kullanın, eğer \"GradientStyle\" almak istiyorsanız,
# \"GradientVariant\" ve \"GradientAngle\" özellikleri belge kaydedildikten sonra.
save_options = aw.saving.OoxmlSaveOptions()
save_options.compliance = aw.saving.OoxmlCompliance.ISO29500_2008_STRICT
doc.save(file_name=ARTIFACTS_DIR + 'Shape.GradientFill.docx', save_options=save_options)
```

### See Also

* module [aspose.words.drawing](../../)
* class [Fill](../)

