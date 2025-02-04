---
title: GradientStop Class
linktitle: GradientStop
articleTitle: GradientStop
second_title: Aspose.Words for .NET
description: Aspose.Words.Drawing.GradientStop class. Represents one gradient stop in C#.
type: docs
weight: 1300
url: /net/aspose.words.drawing/gradientstop/
---
## GradientStop class

Represents one gradient stop.

To learn more, visit the [Working with Graphic Elements](https://docs.aspose.com/words/net/working-with-graphic-elements/) documentation article.

```csharp
public class GradientStop
```

## Constructors

| Name | Description |
| --- | --- |
| [GradientStop](gradientstop/#constructor)(*Color, double*) | Initializes a new instance of the `GradientStop` class. |
| [GradientStop](gradientstop/#constructor_1)(*Color, double, double*) | Initializes a new instance of the `GradientStop` class. |

## Properties

| Name | Description |
| --- | --- |
| [BaseColor](../../aspose.words.drawing/gradientstop/basecolor/) { get; } | Gets a value representing the color of the gradient stop without any modifiers. |
| [Color](../../aspose.words.drawing/gradientstop/color/) { get; set; } | Gets or sets a value representing the color of the gradient stop. |
| [Position](../../aspose.words.drawing/gradientstop/position/) { get; set; } | Gets or sets a value representing the position of a stop within the gradient expressed as a percent in range 0.0 to 1.0. |
| [Transparency](../../aspose.words.drawing/gradientstop/transparency/) { get; set; } | Gets or sets a value representing the transparency of the gradient fill expressed as a percent in range 0.0 to 1.0. |

## Methods

| Name | Description |
| --- | --- |
| [Remove](../../aspose.words.drawing/gradientstop/remove/)() | Removes the gradient stop from the parent [`GradientStopCollection`](../gradientstopcollection/). |

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

Assert.AreEqual(2, gradientStops.Count);

Assert.AreEqual(Color.FromArgb(255, 0, 255, 255), gradientStops[0].BaseColor);
Assert.AreEqual(Color.Aqua.ToArgb(), gradientStops[0].Color.ToArgb());
Assert.AreEqual(0.1d, gradientStops[0].Position, 0.01d);
Assert.AreEqual(0.25d, gradientStops[0].Transparency, 0.01d);

Assert.AreEqual(Color.Chocolate.ToArgb(), gradientStops[1].Color.ToArgb());
Assert.AreEqual(0.75d, gradientStops[1].Position, 0.01d);
Assert.AreEqual(0.3d, gradientStops[1].Transparency, 0.01d);

// Use the compliance option to define the shape using DML
// if you want to get "GradientStops" property after the document saves.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Compliance = OoxmlCompliance.Iso29500_2008_Strict };

doc.Save(ArtifactsDir + "Shape.GradientStops.docx", saveOptions);
```

### See Also

* namespace [Aspose.Words.Drawing](../../aspose.words.drawing/)
* assembly [Aspose.Words](../../)
