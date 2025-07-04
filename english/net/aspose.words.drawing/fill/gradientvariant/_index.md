---
title: Fill.GradientVariant
linktitle: GradientVariant
articleTitle: GradientVariant
second_title: Aspose.Words for .NET
description: Discover how to set the GradientVariant property for stunning fill effects. Enhance your design with vibrant gradient options today!
type: docs
weight: 130
url: /net/aspose.words.drawing/fill/gradientvariant/
---
## Fill.GradientVariant property

Gets the gradient variant [`GradientVariant`](../../gradientvariant/) for the fill.

```csharp
public GradientVariant GradientVariant { get; }
```

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

* enum [GradientVariant](../../gradientvariant/)
* class [Fill](../)
* namespace [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assembly [Aspose.Words](../../../)
