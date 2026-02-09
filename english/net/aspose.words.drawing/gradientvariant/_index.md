---
title: GradientVariant Enum
linktitle: GradientVariant
articleTitle: GradientVariant
second_title: Aspose.Words for .NET
description: Discover the Aspose.Words.Drawing.GradientVariant enum for customizable gradient fills, enhancing your document designs with vibrant styles.
type: docs
weight: 1340
url: /net/aspose.words.drawing/gradientvariant/
---
## GradientVariant enumeration

Specifies the variant for a gradient fill.

```csharp
public enum GradientVariant
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| None | `0` | Gradient variant 'None'. |
| Variant1 | `1` | Gradient variant 1. |
| Variant2 | `2` | Gradient variant 2. |
| Variant3 | `3` | Gradient variant 3. |
| Variant4 | `4` | Gradient variant 4. |

## Remarks

Corresponds to the four variants on the Gradient tab in the Fill Effects dialog box in Word.

## Examples

Shows how to fill a shape with a gradients.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.Rectangle, 80, 80);
// Apply One-color gradient fill to the shape with ForeColor of gradient fill.
shape.Fill.OneColorGradient(Color.Red, GradientStyle.Horizontal, GradientVariant.Variant2, 0.1);

Assert.That(shape.Fill.ForeColor.ToArgb(), Is.EqualTo(Color.Red.ToArgb()));
Assert.That(shape.Fill.GradientStyle, Is.EqualTo(GradientStyle.Horizontal));
Assert.That(shape.Fill.GradientVariant, Is.EqualTo(GradientVariant.Variant2));
Assert.That(shape.Fill.GradientAngle, Is.EqualTo(270));

shape = builder.InsertShape(ShapeType.Rectangle, 80, 80);
// Apply Two-color gradient fill to the shape.
shape.Fill.TwoColorGradient(GradientStyle.FromCorner, GradientVariant.Variant4);
// Change BackColor of gradient fill.
shape.Fill.BackColor = Color.Yellow;
// Note that changes "GradientAngle" for "GradientStyle.FromCorner/GradientStyle.FromCenter"
// gradient fill don't get any effect, it will work only for linear gradient.
shape.Fill.GradientAngle = 15;

Assert.That(shape.Fill.BackColor.ToArgb(), Is.EqualTo(Color.Yellow.ToArgb()));
Assert.That(shape.Fill.GradientStyle, Is.EqualTo(GradientStyle.FromCorner));
Assert.That(shape.Fill.GradientVariant, Is.EqualTo(GradientVariant.Variant4));
Assert.That(shape.Fill.GradientAngle, Is.EqualTo(0));

// Use the compliance option to define the shape using DML if you want to get "GradientStyle",
// "GradientVariant" and "GradientAngle" properties after the document saves.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Compliance = OoxmlCompliance.Iso29500_2008_Strict };

doc.Save(ArtifactsDir + "Shape.GradientFill.docx", saveOptions);
```

### See Also

* namespace [Aspose.Words.Drawing](../../aspose.words.drawing/)
* assembly [Aspose.Words](../../)
