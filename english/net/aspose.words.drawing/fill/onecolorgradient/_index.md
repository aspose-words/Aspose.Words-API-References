---
title: Fill.OneColorGradient
linktitle: OneColorGradient
articleTitle: OneColorGradient
second_title: Aspose.Words for .NET
description: Discover how to use the OneColorGradient method to create stunning one-color gradients for your designs. Enhance your projects effortlessly!
type: docs
weight: 220
url: /net/aspose.words.drawing/fill/onecolorgradient/
---
## OneColorGradient(*[GradientStyle](../../gradientstyle/), [GradientVariant](../../gradientvariant/), double*) {#onecolorgradient}

Sets the specified fill to a one-color gradient.

```csharp
public void OneColorGradient(GradientStyle style, GradientVariant variant, double degree)
```

| Parameter | Type | Description |
| --- | --- | --- |
| style | GradientStyle | The gradient style [`GradientStyle`](../../gradientstyle/) |
| variant | GradientVariant | The gradient variant [`GradientVariant`](../../gradientvariant/) |
| degree | Double | The gradient degree. Can be a value from 0.0 (dark) to 1.0 (light). |

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

* enum [GradientStyle](../../gradientstyle/)
* enum [GradientVariant](../../gradientvariant/)
* class [Fill](../)
* namespace [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assembly [Aspose.Words](../../../)

---

## OneColorGradient(*Color, [GradientStyle](../../gradientstyle/), [GradientVariant](../../gradientvariant/), double*) {#onecolorgradient_1}

Sets the specified fill to a one-color gradient using the specified color.

```csharp
public void OneColorGradient(Color color, GradientStyle style, GradientVariant variant, 
    double degree)
```

| Parameter | Type | Description |
| --- | --- | --- |
| color | Color | The color to build the gradient. |
| style | GradientStyle | The gradient style [`GradientStyle`](../../gradientstyle/) |
| variant | GradientVariant | The gradient variant [`GradientVariant`](../../gradientvariant/) |
| degree | Double | The gradient degree. Can be a value from 0.0 (dark) to 1.0 (light). |

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

* enum [GradientStyle](../../gradientstyle/)
* enum [GradientVariant](../../gradientvariant/)
* class [Fill](../)
* namespace [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assembly [Aspose.Words](../../../)
