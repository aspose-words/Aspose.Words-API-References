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

Assert.AreEqual(2, shapes.Length);

// The two shapes are identical in terms of dimensions and shape type.
Assert.AreEqual(shapes[0].Width, shapes[1].Width);
Assert.AreEqual(shapes[0].Height, shapes[1].Height);
Assert.AreEqual(shapes[0].ShapeType, shapes[1].ShapeType);

// The first shape has no effects, and the second one has a shadow and thick outline.
// These effects make the size of the second shape's silhouette bigger than that of the first.
// Even though the rectangle's size shows up when we click on these shapes in Microsoft Word,
// the visible outer bounds of the second shape are affected by the shadow and outline and thus are bigger.
// We can use the "AdjustWithEffects" method to see the true size of the shape.
Assert.AreEqual(0.0, shapes[0].StrokeWeight);
Assert.AreEqual(20.0, shapes[1].StrokeWeight);
Assert.False(shapes[0].ShadowEnabled);
Assert.True(shapes[1].ShadowEnabled);

Shape shape = shapes[0];

// Create a RectangleF object, representing a rectangle,
// which we could potentially use as the coordinates and bounds for a shape.
RectangleF rectangleF = new RectangleF(200, 200, 1000, 1000);

// Run this method to get the size of the rectangle adjusted for all our shape effects.
RectangleF rectangleFOut = shape.AdjustWithEffects(rectangleF);

// Since the shape has no border-changing effects, its boundary dimensions are unaffected.
Assert.AreEqual(200, rectangleFOut.X);
Assert.AreEqual(200, rectangleFOut.Y);
Assert.AreEqual(1000, rectangleFOut.Width);
Assert.AreEqual(1000, rectangleFOut.Height);

// Verify the final extent of the first shape, in points.
Assert.AreEqual(0, shape.BoundsWithEffects.X);
Assert.AreEqual(0, shape.BoundsWithEffects.Y);
Assert.AreEqual(147, shape.BoundsWithEffects.Width);
Assert.AreEqual(147, shape.BoundsWithEffects.Height);

shape = shapes[1];
rectangleF = new RectangleF(200, 200, 1000, 1000);
rectangleFOut = shape.AdjustWithEffects(rectangleF);

// The shape effects have moved the apparent top left corner of the shape slightly.
Assert.AreEqual(171.5, rectangleFOut.X);
Assert.AreEqual(167, rectangleFOut.Y);

// The effects have also affected the visible dimensions of the shape.
Assert.AreEqual(1045, rectangleFOut.Width);
Assert.AreEqual(1133.5, rectangleFOut.Height);

// The effects have also affected the visible bounds of the shape.
Assert.AreEqual(-28.5, shape.BoundsWithEffects.X);
Assert.AreEqual(-33, shape.BoundsWithEffects.Y);
Assert.AreEqual(192, shape.BoundsWithEffects.Width);
Assert.AreEqual(280.5, shape.BoundsWithEffects.Height);
```

### See Also

* class [ShapeBase](../)
* namespace [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assembly [Aspose.Words](../../../)
