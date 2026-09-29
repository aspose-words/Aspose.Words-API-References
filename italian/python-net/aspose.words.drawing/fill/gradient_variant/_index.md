---
title: Fill.gradient_variant property
linktitle: gradient_variant property
articleTitle: gradient_variant property
second_title: Aspose.Words for Python
description: "Fill.gradient_variant property. Gets the gradient variant [GradientVariant](../../gradientvariant/) for the fill."
type: docs
weight: 130
url: /it/python-net/aspose.words.drawing/fill/gradient_variant/
---

## Fill.gradient_variant property

Gets the gradient variant [GradientVariant](../../gradientvariant/) for the fill.



```python
@property
def gradient_variant(self) -> aspose.words.drawing.GradientVariant:
    ...

```

### Examples

Shows how to fill a shape with a gradients.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
shape = builder.insert_shape(shape_type=aw.drawing.ShapeType.RECTANGLE, width=80, height=80)
# Applica un riempimento a gradiente monocolore alla forma con ForeColor del gradiente.
shape.fill.one_color_gradient(color=aspose.pydrawing.Color.red, style=aw.drawing.GradientStyle.HORIZONTAL, variant=aw.drawing.GradientVariant.VARIANT2, degree=0.1)
self.assertEqual(aspose.pydrawing.Color.red.to_argb(), shape.fill.fore_color.to_argb())
self.assertEqual(aw.drawing.GradientStyle.HORIZONTAL, shape.fill.gradient_style)
self.assertEqual(aw.drawing.GradientVariant.VARIANT2, shape.fill.gradient_variant)
self.assertEqual(270, shape.fill.gradient_angle)
shape = builder.insert_shape(shape_type=aw.drawing.ShapeType.RECTANGLE, width=80, height=80)
# Applica riempimento a gradiente a due colori alla forma.
shape.fill.two_color_gradient(style=aw.drawing.GradientStyle.FROM_CORNER, variant=aw.drawing.GradientVariant.VARIANT4)
# Modifica il BackColor del riempimento a gradiente.
shape.fill.back_color = aspose.pydrawing.Color.yellow
# Nota che le modifiche a "GradientAngle" per "GradientStyle.FromCorner/GradientStyle.FromCenter"
# Il riempimento a gradiente non ha alcun effetto, funzionerà solo per il gradiente lineare.
shape.fill.gradient_angle = 15
self.assertEqual(aspose.pydrawing.Color.yellow.to_argb(), shape.fill.back_color.to_argb())
self.assertEqual(aw.drawing.GradientStyle.FROM_CORNER, shape.fill.gradient_style)
self.assertEqual(aw.drawing.GradientVariant.VARIANT4, shape.fill.gradient_variant)
self.assertEqual(0, shape.fill.gradient_angle)
# Usa l'opzione di conformità per definire la forma usando DML se vuoi ottenere "GradientStyle",
# le proprietà "GradientVariant" e "GradientAngle" dopo che il documento viene salvato.
save_options = aw.saving.OoxmlSaveOptions()
save_options.compliance = aw.saving.OoxmlCompliance.ISO29500_2008_STRICT
doc.save(file_name=ARTIFACTS_DIR + 'Shape.GradientFill.docx', save_options=save_options)
```

### See Also

* module [aspose.words.drawing](../../)
* class [Fill](../)

