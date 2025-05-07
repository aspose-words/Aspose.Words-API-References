---
title: Fill.twoColorGradient method
linktitle: twoColorGradient method
articleTitle: twoColorGradient method
second_title: Aspose.Words for Node.js
description: "Aspose.Words.Drawing.Fill.twoColorGradient method"
type: docs
weight: 270
url: /nodejs-net/aspose.words.drawing/fill/twoColorGradient/
---

## twoColorGradient(style, variant) {#gradientstyle_gradientvariant}

Sets the specified fill to a two-color gradient.


```js
twoColorGradient(style: Aspose.Words.Drawing.GradientStyle, variant: Aspose.Words.Drawing.GradientVariant)
```

| Parameter | Type | Description |
| --- | --- | --- |
| style | [GradientStyle](../../gradientstyle/) | The gradient style [GradientStyle](../../gradientstyle/). |
| variant | [GradientVariant](../../gradientvariant/) | The gradient variant [GradientVariant](../../gradientvariant/) |

## twoColorGradient(color1, color2, style, variant) {#string_string_gradientstyle_gradientvariant}

Sets the specified fill to a two-color gradient.


```js
twoColorGradient(color1: string, color2: string, style: Aspose.Words.Drawing.GradientStyle, variant: Aspose.Words.Drawing.GradientVariant)
```

| Parameter | Type | Description |
| --- | --- | --- |
| color1 | string | The first color to build the gradient. |
| color2 | string | The second color to build the gradient. |
| style | [GradientStyle](../../gradientstyle/) | The gradient style [GradientStyle](../../gradientstyle/). |
| variant | [GradientVariant](../../gradientvariant/) | The gradient variant [GradientVariant](../../gradientvariant/) |

## Examples

Shows how to fill a shape with a gradients.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

let shape = builder.insertShape(aw.Drawing.ShapeType.Rectangle, 80, 80);
// Apply One-color gradient fill to the shape with ForeColor of gradient fill.
shape.fill.oneColorGradient("#FF0000", aw.Drawing.GradientStyle.Horizontal, aw.Drawing.GradientVariant.Variant2, 0.1);

expect(shape.fill.foreColor).toEqual("#FF0000");
expect(shape.fill.gradientStyle).toEqual(aw.Drawing.GradientStyle.Horizontal);
expect(shape.fill.gradientVariant).toEqual(aw.Drawing.GradientVariant.Variant2);
expect(shape.fill.gradientAngle).toEqual(270);

shape = builder.insertShape(aw.Drawing.ShapeType.Rectangle, 80, 80);
// Apply Two-color gradient fill to the shape.
shape.fill.twoColorGradient(aw.Drawing.GradientStyle.FromCorner, aw.Drawing.GradientVariant.Variant4);
// Change BackColor of gradient fill.
shape.fill.backColor = "#FFFF00";
// Note that changes "GradientAngle" for "GradientStyle.FromCorner/aw.Drawing.GradientStyle.FromCenter"
// gradient fill don't get any effect, it will work only for linear gradient.
shape.fill.gradientAngle = 15;

expect(shape.fill.backColor).toEqual("#FFFF00");
expect(shape.fill.gradientStyle).toEqual(aw.Drawing.GradientStyle.FromCorner);
expect(shape.fill.gradientVariant).toEqual(aw.Drawing.GradientVariant.Variant4);
expect(shape.fill.gradientAngle).toEqual(0);

// Use the compliance option to define the shape using DML if you want to get "GradientStyle",
// "GradientVariant" and "GradientAngle" properties after the document saves.
let saveOptions = new aw.Saving.OoxmlSaveOptions();
saveOptions.compliance = aw.Saving.OoxmlCompliance.Iso29500_2008_Strict;

doc.save(base.artifactsDir + "Shape.gradientFill.docx", saveOptions);
```

## See Also

* module [Aspose.Words.Drawing](../../)
* class [Fill](../)

