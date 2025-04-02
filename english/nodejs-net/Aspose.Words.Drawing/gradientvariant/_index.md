---
title: GradientVariant enumeration
linktitle: GradientVariant enumeration
articleTitle: GradientVariant enumeration
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.Drawing.GradientVariant enumeration. Specifies the variant for a gradient fill."
type: docs
weight: 160
url: /nodejs-net/Aspose.Words.Drawing/gradientvariant/
---

## GradientVariant enumeration

Specifies the variant for a gradient fill.

Corresponds to the four variants on the Gradient tab in the Fill Effects dialog box in Word.


### Members

| Name | Description |
| --- | --- |
| None | Gradient variant 'None'. |
| Variant1 | Gradient variant 1. |
| Variant2 | Gradient variant 2. |
| Variant3 | Gradient variant 3. |
| Variant4 | Gradient variant 4. |

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

### See Also

* module [Aspose.Words.Drawing](../)

