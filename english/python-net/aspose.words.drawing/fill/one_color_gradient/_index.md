---
title: Fill.one_color_gradient method
linktitle: one_color_gradient method
articleTitle: one_color_gradient method
second_title: Aspose.Words for Python
description: "aspose.words.drawing.Fill.one_color_gradient method"
type: docs
weight: 220
url: /python-net/aspose.words.drawing/fill/one_color_gradient/
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
builder = aw.DocumentBuilder(doc)

shape = builder.insert_shape(aw.drawing.ShapeType.RECTANGLE, 80, 80)
# Apply One-color gradient fill to the shape with "fore_color" of gradient fill.
shape.fill.one_color_gradient(drawing.Color.red, aw.drawing.GradientStyle.HORIZONTAL, aw.drawing.GradientVariant.VARIANT2, 0.1)

self.assertEqual(drawing.Color.red.to_argb(), shape.fill.fore_color.to_argb())
self.assertEqual(aw.drawing.GradientStyle.HORIZONTAL, shape.fill.gradient_style)
self.assertEqual(aw.drawing.GradientVariant.VARIANT2, shape.fill.gradient_variant)
self.assertEqual(270, shape.fill.gradient_angle)

shape = builder.insert_shape(aw.drawing.ShapeType.RECTANGLE, 80, 80)
# Apply Two-color gradient fill to the shape.
shape.fill.two_color_gradient(aw.drawing.GradientStyle.FROM_CORNER, aw.drawing.GradientVariant.VARIANT4)
# Change "back_color" of gradient fill.
shape.fill.back_color = drawing.Color.yellow
# Note that changes "gradient_angle" for "GradientStyle.FROM_CORNER/GradientStyle.FROM_CENTER"
# gradient fill don't get any effect, it will work only for linear gradient.
shape.fill.gradient_angle = 15

self.assertEqual(drawing.Color.yellow.to_argb(), shape.fill.back_color.to_argb())
self.assertEqual(aw.drawing.GradientStyle.FROM_CORNER, shape.fill.gradient_style)
self.assertEqual(aw.drawing.GradientVariant.VARIANT4, shape.fill.gradient_variant)
self.assertEqual(0, shape.fill.gradient_angle)

# Use the compliance option to define the shape using DML if you want to get "gradient_style",
# "gradient_variant" and "gradient_angle" properties after the document saves.
save_options = aw.saving.OoxmlSaveOptions()
save_options.compliance = aw.saving.OoxmlCompliance.ISO29500_2008_STRICT

doc.save(ARTIFACTS_DIR + "Shape.gradient_fill.docx", save_options)
```

## See Also

* module [aspose.words.drawing](../../)
* class [Fill](../)

