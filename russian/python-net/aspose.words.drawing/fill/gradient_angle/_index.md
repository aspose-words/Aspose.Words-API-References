---
title: Fill.gradient_angle property
linktitle: gradient_angle property
articleTitle: gradient_angle property
second_title: Aspose.Words for Python
description: "Fill.gradient_angle property. Gets or sets the angle of the gradient fill."
type: docs
weight: 100
url: /ru/python-net/aspose.words.drawing/fill/gradient_angle/
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
# Применить одноцветную градиентную заливку к фигуре с ForeColor градиентной заливки.
shape.fill.one_color_gradient(color=aspose.pydrawing.Color.red, style=aw.drawing.GradientStyle.HORIZONTAL, variant=aw.drawing.GradientVariant.VARIANT2, degree=0.1)
self.assertEqual(aspose.pydrawing.Color.red.to_argb(), shape.fill.fore_color.to_argb())
self.assertEqual(aw.drawing.GradientStyle.HORIZONTAL, shape.fill.gradient_style)
self.assertEqual(aw.drawing.GradientVariant.VARIANT2, shape.fill.gradient_variant)
self.assertEqual(270, shape.fill.gradient_angle)
shape = builder.insert_shape(shape_type=aw.drawing.ShapeType.RECTANGLE, width=80, height=80)
# Применить двухцветную градиентную заливку к фигуре.
shape.fill.two_color_gradient(style=aw.drawing.GradientStyle.FROM_CORNER, variant=aw.drawing.GradientVariant.VARIANT4)
# Изменить BackColor градиентной заливки.
shape.fill.back_color = aspose.pydrawing.Color.yellow
# Обратите внимание, что изменения "GradientAngle" для "GradientStyle.FromCorner/GradientStyle.FromCenter"
# Градиентная заливка не оказывает эффекта, она будет работать только для линейного градиента.
shape.fill.gradient_angle = 15
self.assertEqual(aspose.pydrawing.Color.yellow.to_argb(), shape.fill.back_color.to_argb())
self.assertEqual(aw.drawing.GradientStyle.FROM_CORNER, shape.fill.gradient_style)
self.assertEqual(aw.drawing.GradientVariant.VARIANT4, shape.fill.gradient_variant)
self.assertEqual(0, shape.fill.gradient_angle)
# Используйте параметр compliance, чтобы определить фигуру с помощью DML, если вы хотите получить "GradientStyle",
# "GradientVariant" и свойства "GradientAngle" после сохранения документа.
save_options = aw.saving.OoxmlSaveOptions()
save_options.compliance = aw.saving.OoxmlCompliance.ISO29500_2008_STRICT
doc.save(file_name=ARTIFACTS_DIR + 'Shape.GradientFill.docx', save_options=save_options)
```

### See Also

* module [aspose.words.drawing](../../)
* class [Fill](../)

