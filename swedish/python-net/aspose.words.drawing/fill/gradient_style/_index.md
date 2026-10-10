---
title: Fill.gradient_style property
linktitle: gradient_style property
articleTitle: gradient_style property
second_title: Aspose.Words for Python
description: "Fill.gradient_style property. Gets the gradient style [GradientStyle](../../gradientstyle/) for the fill."
type: docs
weight: 120
url: /sv/python-net/aspose.words.drawing/fill/gradient_style/
---

## Fill.gradient_style property

Gets the gradient style [GradientStyle](../../gradientstyle/) for the fill.



```python
@property
def gradient_style(self) -> aspose.words.drawing.GradientStyle:
    ...

```

### Examples

Shows how to fill a shape with a gradients.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
shape = builder.insert_shape(shape_type=aw.drawing.ShapeType.RECTANGLE, width=80, height=80)
# Applicera enfärgad gradientfyllning på formen med förgrundsfärgen för gradientfyllning.
shape.fill.one_color_gradient(color=aspose.pydrawing.Color.red, style=aw.drawing.GradientStyle.HORIZONTAL, variant=aw.drawing.GradientVariant.VARIANT2, degree=0.1)
self.assertEqual(aspose.pydrawing.Color.red.to_argb(), shape.fill.fore_color.to_argb())
self.assertEqual(aw.drawing.GradientStyle.HORIZONTAL, shape.fill.gradient_style)
self.assertEqual(aw.drawing.GradientVariant.VARIANT2, shape.fill.gradient_variant)
self.assertEqual(270, shape.fill.gradient_angle)
shape = builder.insert_shape(shape_type=aw.drawing.ShapeType.RECTANGLE, width=80, height=80)
# Applicera tvåfärgsgradientfyllning på formen.
shape.fill.two_color_gradient(style=aw.drawing.GradientStyle.FROM_CORNER, variant=aw.drawing.GradientVariant.VARIANT4)
# Ändra BackColor för gradientfyllning.
shape.fill.back_color = aspose.pydrawing.Color.yellow
# Observera att ändringar av "GradientAngle" för "GradientStyle.FromCorner/GradientStyle.FromCenter"
# gradientfyllning har ingen effekt, den fungerar bara för linjär gradient.
shape.fill.gradient_angle = 15
self.assertEqual(aspose.pydrawing.Color.yellow.to_argb(), shape.fill.back_color.to_argb())
self.assertEqual(aw.drawing.GradientStyle.FROM_CORNER, shape.fill.gradient_style)
self.assertEqual(aw.drawing.GradientVariant.VARIANT4, shape.fill.gradient_variant)
self.assertEqual(0, shape.fill.gradient_angle)
# Använd efterlevnadsalternativet för att definiera formen med DML om du vill få "GradientStyle",
# "GradientVariant" och "GradientAngle" egenskaper efter att dokumentet sparas.
save_options = aw.saving.OoxmlSaveOptions()
save_options.compliance = aw.saving.OoxmlCompliance.ISO29500_2008_STRICT
doc.save(file_name=ARTIFACTS_DIR + 'Shape.GradientFill.docx', save_options=save_options)
```

### See Also

* module [aspose.words.drawing](../../)
* class [Fill](../)

