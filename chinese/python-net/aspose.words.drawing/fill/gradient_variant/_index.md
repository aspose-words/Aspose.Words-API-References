---
title: Fill.gradient_variant property
linktitle: gradient_variant property
articleTitle: gradient_variant property
second_title: Aspose.Words for Python
description: "Fill.gradient_variant property. Gets the gradient variant [GradientVariant](../../gradientvariant/) for the fill."
type: docs
weight: 130
url: /zh/python-net/aspose.words.drawing/fill/gradient_variant/
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
# 对形状应用单色渐变填充，使用渐变填充的前景色。
shape.fill.one_color_gradient(color=aspose.pydrawing.Color.red, style=aw.drawing.GradientStyle.HORIZONTAL, variant=aw.drawing.GradientVariant.VARIANT2, degree=0.1)
self.assertEqual(aspose.pydrawing.Color.red.to_argb(), shape.fill.fore_color.to_argb())
self.assertEqual(aw.drawing.GradientStyle.HORIZONTAL, shape.fill.gradient_style)
self.assertEqual(aw.drawing.GradientVariant.VARIANT2, shape.fill.gradient_variant)
self.assertEqual(270, shape.fill.gradient_angle)
shape = builder.insert_shape(shape_type=aw.drawing.ShapeType.RECTANGLE, width=80, height=80)
# 对形状应用双色渐变填充。
shape.fill.two_color_gradient(style=aw.drawing.GradientStyle.FROM_CORNER, variant=aw.drawing.GradientVariant.VARIANT4)
# 更改渐变填充的背景颜色。
shape.fill.back_color = aspose.pydrawing.Color.yellow
# 注意对 "GradientAngle" 的更改适用于 "GradientStyle.FromCorner/GradientStyle.FromCenter"
# 渐变填充没有任何效果，它仅对线性渐变有效。
shape.fill.gradient_angle = 15
self.assertEqual(aspose.pydrawing.Color.yellow.to_argb(), shape.fill.back_color.to_argb())
self.assertEqual(aw.drawing.GradientStyle.FROM_CORNER, shape.fill.gradient_style)
self.assertEqual(aw.drawing.GradientVariant.VARIANT4, shape.fill.gradient_variant)
self.assertEqual(0, shape.fill.gradient_angle)
# 如果想获取 "GradientStyle"，请使用合规选项通过 DML 定义形状，
# 在文档保存后，"GradientVariant" 和 "GradientAngle" 属性。
save_options = aw.saving.OoxmlSaveOptions()
save_options.compliance = aw.saving.OoxmlCompliance.ISO29500_2008_STRICT
doc.save(file_name=ARTIFACTS_DIR + 'Shape.GradientFill.docx', save_options=save_options)
```

### See Also

* module [aspose.words.drawing](../../)
* class [Fill](../)

