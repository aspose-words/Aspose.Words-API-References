---
title: GradientStyle Enum
linktitle: GradientStyle
articleTitle: GradientStyle
second_title: Aspose.Words for .NET
description: Aspose.Words.Drawing.GradientStyle enum. Specifies the style for a gradient fill in C#.
type: docs
weight: 1160
url: /net/aspose.words.drawing/gradientstyle/
---
## GradientStyle enumeration

Specifies the style for a gradient fill.

```csharp
public enum GradientStyle
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| None | `-1` | No gradient. |
| Horizontal | `1` | Gradient running horizontally across an object. |
| Vertical | `2` | Gradient running vertically down an object. |
| DiagonalUp | `3` | Diagonal gradient moving from a bottom corner up to the opposite corner. |
| DiagonalDown | `4` | Diagonal gradient moving from a top corner down to the opposite corner. |
| FromCorner | `5` | Gradient running from a corner to the other three corners. |
| FromCenter | `6` | Gradient running from the center out to the corners. |

## Examples

Shows how to fill a shape with a gradients.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.Rectangle, 80, 80);
// Apply One-color gradient fill to the shape with ForeColor of gradient fill.
shape.Fill.OneColorGradient(Color.Red, GradientStyle.Horizontal, GradientVariant.Variant2, 0.1);

Assert.AreEqual(Color.Red.ToArgb(), shape.Fill.ForeColor.ToArgb());
Assert.AreEqual(GradientStyle.Horizontal, shape.Fill.GradientStyle);
Assert.AreEqual(GradientVariant.Variant2, shape.Fill.GradientVariant);
Assert.AreEqual(270, shape.Fill.GradientAngle);

shape = builder.InsertShape(ShapeType.Rectangle, 80, 80);
// Apply Two-color gradient fill to the shape.
shape.Fill.TwoColorGradient(GradientStyle.FromCorner, GradientVariant.Variant4);
// Change BackColor of gradient fill.
shape.Fill.BackColor = Color.Yellow;
// Note that changes "GradientAngle" for "GradientStyle.FromCorner/GradientStyle.FromCenter"
// gradient fill don't get any effect, it will work only for linear gradient.
shape.Fill.GradientAngle = 15;

Assert.AreEqual(Color.Yellow.ToArgb(), shape.Fill.BackColor.ToArgb());
Assert.AreEqual(GradientStyle.FromCorner, shape.Fill.GradientStyle);
Assert.AreEqual(GradientVariant.Variant4, shape.Fill.GradientVariant);
Assert.AreEqual(0, shape.Fill.GradientAngle);

// Use the compliance option to define the shape using DML if you want to get "GradientStyle",
// "GradientVariant" and "GradientAngle" properties after the document saves.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Compliance = OoxmlCompliance.Iso29500_2008_Strict };

doc.Save(ArtifactsDir + "Shape.GradientFill.docx", saveOptions);
```

### See Also

* namespace [Aspose.Words.Drawing](../../aspose.words.drawing/)
* assembly [Aspose.Words](../../)
