---
title: ShapeBase.AdjustWithEffects
linktitle: AdjustWithEffects
articleTitle: AdjustWithEffects
second_title: Aspose.Words for .NET
description: Discover how the ShapeBase AdjustWithEffects method enhances your source rectangle by adding effect extents, delivering precise final rectangle values.
type: docs
weight: 660
url: /net/aspose.words.drawing/shapebase/adjustwitheffects/
---
## ShapeBase.AdjustWithEffects method

Adds to the source rectangle values of the effect extent and returns the final rectangle.

```csharp
public RectangleF AdjustWithEffects(RectangleF source)
```

## Examples

Shows how to check how a shape's bounds are affected by shape effects.

```csharp
Document doc = new Document(MyDir + "Shape shadow effect.docx");

Shape[] shapes = doc.GetChildNodes(NodeType.Shape, true).OfType<Shape>().ToArray();

Assert.That(shapes.Length, Is.EqualTo(2));

// The two shapes are identical in terms of dimensions and shape type.
Assert.That(shapes[1].Width, Is.EqualTo(shapes[0].Width));
Assert.That(shapes[1].Height, Is.EqualTo(shapes[0].Height));
Assert.That(shapes[1].ShapeType, Is.EqualTo(shapes[0].ShapeType));

// The first shape has no effects, and the second one has a shadow and thick outline.
// These effects make the size of the second shape's silhouette bigger than that of the first.
// Even though the rectangle's size shows up when we click on these shapes in Microsoft Word,
// the visible outer bounds of the second shape are affected by the shadow and outline and thus are bigger.
// We can use the "AdjustWithEffects" method to see the true size of the shape.
Assert.That(shapes[0].StrokeWeight, Is.EqualTo(0.0));
Assert.That(shapes[1].StrokeWeight, Is.EqualTo(20.0));
Assert.That(shapes[0].ShadowEnabled, Is.False);
Assert.That(shapes[1].ShadowEnabled, Is.True);

Shape shape = shapes[0];

// Create a RectangleF object, representing a rectangle,
// which we could potentially use as the coordinates and bounds for a shape.
RectangleF rectangleF = new RectangleF(200, 200, 1000, 1000);

// Run this method to get the size of the rectangle adjusted for all our shape effects.
RectangleF rectangleFOut = shape.AdjustWithEffects(rectangleF);

// Since the shape has no border-changing effects, its boundary dimensions are unaffected.
Assert.That(rectangleFOut.X, Is.EqualTo(200));
Assert.That(rectangleFOut.Y, Is.EqualTo(200));
Assert.That(rectangleFOut.Width, Is.EqualTo(1000));
Assert.That(rectangleFOut.Height, Is.EqualTo(1000));

// Verify the final extent of the first shape, in points.
Assert.That(shape.BoundsWithEffects.X, Is.EqualTo(0));
Assert.That(shape.BoundsWithEffects.Y, Is.EqualTo(0));
Assert.That(shape.BoundsWithEffects.Width, Is.EqualTo(147));
Assert.That(shape.BoundsWithEffects.Height, Is.EqualTo(147));

shape = shapes[1];
rectangleF = new RectangleF(200, 200, 1000, 1000);
rectangleFOut = shape.AdjustWithEffects(rectangleF);

// The shape effects have moved the apparent top left corner of the shape slightly.
Assert.That(rectangleFOut.X, Is.EqualTo(171.5));
Assert.That(rectangleFOut.Y, Is.EqualTo(167));

// The effects have also affected the visible dimensions of the shape.
Assert.That(rectangleFOut.Width, Is.EqualTo(1045));
Assert.That(rectangleFOut.Height, Is.EqualTo(1133.5));

// The effects have also affected the visible bounds of the shape.
Assert.That(shape.BoundsWithEffects.X, Is.EqualTo(-28.5));
Assert.That(shape.BoundsWithEffects.Y, Is.EqualTo(-33));
Assert.That(shape.BoundsWithEffects.Width, Is.EqualTo(192));
Assert.That(shape.BoundsWithEffects.Height, Is.EqualTo(280.5));
```

### See Also

* class [ShapeBase](../)
* namespace [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assembly [Aspose.Words](../../../)
