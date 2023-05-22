---
title: GradientStyle enumeration
linktitle: GradientStyle enumeration
articleTitle: GradientStyle enumeration
second_title: Aspose.Words for Python
description: "aspose.words.drawing.GradientStyle enumeration. Specifies the style for a gradient fill."
type: docs
weight: 110
url: /python-net/aspose.words.drawing/gradientstyle/
---

## GradientStyle enumeration

Specifies the style for a gradient fill.


### Members

| Name | Description |
| --- | --- |
| NONE | No gradient. |
| HORIZONTAL | Gradient running horizontally across an object. |
| VERTICAL | Gradient running vertically down an object. |
| DIAGONAL_UP | Diagonal gradient moving from a bottom corner up to the opposite corner. |
| DIAGONAL_DOWN | Diagonal gradient moving from a top corner down to the opposite corner. |
| FROM_CORNER | Gradient running from a corner to the other three corners. |
| FROM_CENTER | Gradient running from the center out to the corners. |

### Examples

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

### See Also

* module [aspose.words.drawing](../)

