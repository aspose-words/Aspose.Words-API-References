---
title: Fill.GradientStops
linktitle: GradientStops
articleTitle: GradientStops
second_title: Aspose.Words for .NET
description: Discover how to enhance your designs with the GradientStops property, featuring a collection of GradientStop objects for stunning fill effects.
type: docs
weight: 110
url: /net/aspose.words.drawing/fill/gradientstops/
---
## Fill.GradientStops property

Gets a collection of [`GradientStop`](../../gradientstop/) objects for the fill.

```csharp
public GradientStopCollection GradientStops { get; }
```

## Examples

Shows how to add gradient stops to the gradient fill.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.Rectangle, 80, 80);
shape.Fill.TwoColorGradient(Color.Green, Color.Red, GradientStyle.Horizontal, GradientVariant.Variant2);

// Get gradient stops collection.
GradientStopCollection gradientStops = shape.Fill.GradientStops;

// Change first gradient stop.
gradientStops[0].Color = Color.Aqua;
gradientStops[0].Position = 0.1;
gradientStops[0].Transparency = 0.25;

// Add new gradient stop to the end of collection.
GradientStop gradientStop = new GradientStop(Color.Brown, 0.5);
gradientStops.Add(gradientStop);

// Remove gradient stop at index 1.
gradientStops.RemoveAt(1);
// And insert new gradient stop at the same index 1.
gradientStops.Insert(1, new GradientStop(Color.Chocolate, 0.75, 0.3));

// Remove last gradient stop in the collection.
gradientStop = gradientStops[2];
gradientStops.Remove(gradientStop);

Assert.That(gradientStops.Count, Is.EqualTo(2));

Assert.That(gradientStops[0].BaseColor, Is.EqualTo(Color.FromArgb(255, 0, 255, 255)));
Assert.That(gradientStops[0].Color.ToArgb(), Is.EqualTo(Color.Aqua.ToArgb()));
Assert.That(gradientStops[0].Position, Is.EqualTo(0.1d).Within(0.01d));
Assert.That(gradientStops[0].Transparency, Is.EqualTo(0.25d).Within(0.01d));

Assert.That(gradientStops[1].Color.ToArgb(), Is.EqualTo(Color.Chocolate.ToArgb()));
Assert.That(gradientStops[1].Position, Is.EqualTo(0.75d).Within(0.01d));
Assert.That(gradientStops[1].Transparency, Is.EqualTo(0.3d).Within(0.01d));

// Use the compliance option to define the shape using DML
// if you want to get "GradientStops" property after the document saves.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Compliance = OoxmlCompliance.Iso29500_2008_Strict };

doc.Save(ArtifactsDir + "Shape.GradientStops.docx", saveOptions);
```

### See Also

* class [GradientStopCollection](../../gradientstopcollection/)
* class [Fill](../)
* namespace [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assembly [Aspose.Words](../../../)
