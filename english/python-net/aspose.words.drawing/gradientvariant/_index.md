---
title: GradientVariant enumeration
linktitle: GradientVariant enumeration
articleTitle: GradientVariant enumeration
second_title: Aspose.Words for Python
description: "aspose.words.drawing.GradientVariant enumeration. Specifies the variant for a gradient fill."
type: docs
weight: 120
url: /python-net/aspose.words.drawing/gradientvariant/
---

## GradientVariant enumeration

Specifies the variant for a gradient fill.

Corresponds to the four variants on the Gradient tab in the Fill Effects dialog box in Word.


### Members

| Name | Description |
| --- | --- |
| NONE | Gradient variant 'None'. |
| VARIANT1 | Gradient variant 1. |
| VARIANT2 | Gradient variant 2. |
| VARIANT3 | Gradient variant 3. |
| VARIANT4 | Gradient variant 4. |

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

