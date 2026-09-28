---
title: GradientVariant enumeration
linktitle: GradientVariant enumeration
articleTitle: GradientVariant enumeration
second_title: Aspose.Words for Python
description: "aspose.words.drawing.GradientVariant enumeration. Specifies the variant for a gradient fill."
type: docs
weight: 150
url: /de/python-net/aspose.words.drawing/gradientvariant/
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
builder = aw.DocumentBuilder(doc=doc)
shape = builder.insert_shape(shape_type=aw.drawing.ShapeType.RECTANGLE, width=80, height=80)
# Einfarbige Farbverlauffüllung auf die Form mit ForeColor des Farbverlaufs anwenden.
shape.fill.one_color_gradient(color=aspose.pydrawing.Color.red, style=aw.drawing.GradientStyle.HORIZONTAL, variant=aw.drawing.GradientVariant.VARIANT2, degree=0.1)
self.assertEqual(aspose.pydrawing.Color.red.to_argb(), shape.fill.fore_color.to_argb())
self.assertEqual(aw.drawing.GradientStyle.HORIZONTAL, shape.fill.gradient_style)
self.assertEqual(aw.drawing.GradientVariant.VARIANT2, shape.fill.gradient_variant)
self.assertEqual(270, shape.fill.gradient_angle)
shape = builder.insert_shape(shape_type=aw.drawing.ShapeType.RECTANGLE, width=80, height=80)
# Zweifarbige Farbverlauffüllung auf die Form anwenden.
shape.fill.two_color_gradient(style=aw.drawing.GradientStyle.FROM_CORNER, variant=aw.drawing.GradientVariant.VARIANT4)
# Ändern Sie BackColor des Farbverlaufs.
shape.fill.back_color = aspose.pydrawing.Color.yellow
# Beachten Sie, dass Änderungen an "GradientAngle" für "GradientStyle.FromCorner/GradientStyle.FromCenter"
# Die Farbverlauffüllung hat keine Wirkung, sie funktioniert nur für lineare Verläufe.
shape.fill.gradient_angle = 15
self.assertEqual(aspose.pydrawing.Color.yellow.to_argb(), shape.fill.back_color.to_argb())
self.assertEqual(aw.drawing.GradientStyle.FROM_CORNER, shape.fill.gradient_style)
self.assertEqual(aw.drawing.GradientVariant.VARIANT4, shape.fill.gradient_variant)
self.assertEqual(0, shape.fill.gradient_angle)
# Verwenden Sie die Compliance-Option, um die Form mit DML zu definieren, wenn Sie "GradientStyle" erhalten möchten,
# "GradientVariant"- und "GradientAngle"-Eigenschaften nach dem Speichern des Dokuments.
save_options = aw.saving.OoxmlSaveOptions()
save_options.compliance = aw.saving.OoxmlCompliance.ISO29500_2008_STRICT
doc.save(file_name=ARTIFACTS_DIR + 'Shape.GradientFill.docx', save_options=save_options)
```

### See Also

* module [aspose.words.drawing](../)

