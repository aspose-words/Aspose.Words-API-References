﻿---
title: GradientStyle enumeration
linktitle: GradientStyle enumeration
articleTitle: GradientStyle enumeration
second_title: Aspose.Words for Node.js
description: "Aspose.Words.Drawing.GradientStyle enumeration. Specifies the style for a gradient fill."
type: docs
weight: 150
url: /nodejs-net/aspose.words.drawing/gradientstyle/
---

## GradientStyle enumeration

Specifies the style for a gradient fill.


### Members

| Name | Description |
| --- | --- |
| None | No gradient. |
| Horizontal | Gradient running horizontally across an object. |
| Vertical | Gradient running vertically down an object. |
| DiagonalUp | Diagonal gradient moving from a bottom corner up to the opposite corner. |
| DiagonalDown | Diagonal gradient moving from a top corner down to the opposite corner. |
| FromCorner | Gradient running from a corner to the other three corners. |
| FromCenter | Gradient running from the center out to the corners. |

### Examples

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
// Note that changes "GradientAngle" for "GradientStyle.FromCorner/GradientStyle.FromCenter"
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

### See Also

* module [Aspose.Words.Drawing](../)

