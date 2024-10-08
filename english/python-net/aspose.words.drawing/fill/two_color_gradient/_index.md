﻿---
title: Fill.two_color_gradient method
linktitle: two_color_gradient method
articleTitle: two_color_gradient method
second_title: Aspose.Words for Python
description: "aspose.words.drawing.Fill.two_color_gradient method"
type: docs
weight: 270
url: /python-net/aspose.words.drawing/fill/two_color_gradient/
---

## two_color_gradient(style, variant) {#gradientstyle_gradientvariant}

Sets the specified fill to a two-color gradient.


```python
def two_color_gradient(self, style: aspose.words.drawing.GradientStyle, variant: aspose.words.drawing.GradientVariant):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| style | [GradientStyle](../../gradientstyle/) | The gradient style [GradientStyle](../../gradientstyle/). |
| variant | [GradientVariant](../../gradientvariant/) | The gradient variant [GradientVariant](../../gradientvariant/) |

## two_color_gradient(color1, color2, style, variant) {#color_color_gradientstyle_gradientvariant}

Sets the specified fill to a two-color gradient.


```python
def two_color_gradient(self, color1: aspose.pydrawing.Color, color2: aspose.pydrawing.Color, style: aspose.words.drawing.GradientStyle, variant: aspose.words.drawing.GradientVariant):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| color1 | aspose.pydrawing.Color | The first color to build the gradient. |
| color2 | aspose.pydrawing.Color | The second color to build the gradient. |
| style | [GradientStyle](../../gradientstyle/) | The gradient style [GradientStyle](../../gradientstyle/). |
| variant | [GradientVariant](../../gradientvariant/) | The gradient variant [GradientVariant](../../gradientvariant/) |

## Examples

Shows how to fill a shape with a gradients.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
shape = builder.insert_shape(shape_type=aw.drawing.ShapeType.RECTANGLE, width=80, height=80)
# Apply One-color gradient fill to the shape with ForeColor of gradient fill.
shape.fill.one_color_gradient(color=aspose.pydrawing.Color.red, style=aw.drawing.GradientStyle.HORIZONTAL, variant=aw.drawing.GradientVariant.VARIANT2, degree=0.1)
self.assertEqual(aspose.pydrawing.Color.red.to_argb(), shape.fill.fore_color.to_argb())
self.assertEqual(aw.drawing.GradientStyle.HORIZONTAL, shape.fill.gradient_style)
self.assertEqual(aw.drawing.GradientVariant.VARIANT2, shape.fill.gradient_variant)
self.assertEqual(270, shape.fill.gradient_angle)
shape = builder.insert_shape(shape_type=aw.drawing.ShapeType.RECTANGLE, width=80, height=80)
# Apply Two-color gradient fill to the shape.
shape.fill.two_color_gradient(style=aw.drawing.GradientStyle.FROM_CORNER, variant=aw.drawing.GradientVariant.VARIANT4)
# Change BackColor of gradient fill.
shape.fill.back_color = aspose.pydrawing.Color.yellow
# Note that changes "GradientAngle" for "GradientStyle.FromCorner/GradientStyle.FromCenter"
# gradient fill don't get any effect, it will work only for linear gradient.
shape.fill.gradient_angle = 15
self.assertEqual(aspose.pydrawing.Color.yellow.to_argb(), shape.fill.back_color.to_argb())
self.assertEqual(aw.drawing.GradientStyle.FROM_CORNER, shape.fill.gradient_style)
self.assertEqual(aw.drawing.GradientVariant.VARIANT4, shape.fill.gradient_variant)
self.assertEqual(0, shape.fill.gradient_angle)
# Use the compliance option to define the shape using DML if you want to get "GradientStyle",
# "GradientVariant" and "GradientAngle" properties after the document saves.
save_options = aw.saving.OoxmlSaveOptions()
save_options.compliance = aw.saving.OoxmlCompliance.ISO29500_2008_STRICT
doc.save(file_name=ARTIFACTS_DIR + 'Shape.GradientFill.docx', save_options=save_options)
```

## See Also

* module [aspose.words.drawing](../../)
* class [Fill](../)

