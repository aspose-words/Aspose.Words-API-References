---
title: NodeRendererBase.BoundsInPoints
linktitle: BoundsInPoints
articleTitle: BoundsInPoints
second_title: Aspose.Words for .NET
description: Discover the NodeRendererBase BoundsInPoints property to access precise shape dimensions in points, enhancing your design accuracy and efficiency.
type: docs
weight: 10
url: /net/aspose.words.rendering/noderendererbase/boundsinpoints/
---
## NodeRendererBase.BoundsInPoints property

Gets the actual bounds of the shape in points.

```csharp
public RectangleF BoundsInPoints { get; }
```

## Remarks

This property returns the actual (as rendered on the page) bounding box of the shape. The bounds takes into account shape rotation (if any).

## Examples

Shows how to measure and scale shapes.

```csharp
Document doc = new Document(MyDir + "Office math.docx");

OfficeMath officeMath = (OfficeMath)doc.GetChild(NodeType.OfficeMath, 0, true);
OfficeMathRenderer renderer = new OfficeMathRenderer(officeMath);

// Verify the size of the image that the OfficeMath object will create when we render it.
Assert.AreEqual(122.0f, renderer.SizeInPoints.Width, 0.25f);
Assert.AreEqual(13.0f, renderer.SizeInPoints.Height, 0.15f);

Assert.AreEqual(122.0f, renderer.BoundsInPoints.Width, 0.25f);
Assert.AreEqual(13.0f, renderer.BoundsInPoints.Height, 0.15f);

// Shapes with transparent parts may contain different values in the "OpaqueBoundsInPoints" properties.
Assert.AreEqual(122.0f, renderer.OpaqueBoundsInPoints.Width, 0.25f);
Assert.AreEqual(14.2f, renderer.OpaqueBoundsInPoints.Height, 0.1f);

// Get the shape size in pixels, with linear scaling to a specific DPI.
Rectangle bounds = renderer.GetBoundsInPixels(1.0f, 96.0f);

Assert.AreEqual(163, bounds.Width);
Assert.AreEqual(18, bounds.Height);

// Get the shape size in pixels, but with a different DPI for the horizontal and vertical dimensions.
bounds = renderer.GetBoundsInPixels(1.0f, 96.0f, 150.0f);
Assert.AreEqual(163, bounds.Width);
Assert.AreEqual(27, bounds.Height);

// The opaque bounds may vary here also.
bounds = renderer.GetOpaqueBoundsInPixels(1.0f, 96.0f);

Assert.AreEqual(163, bounds.Width);
Assert.AreEqual(19, bounds.Height);

bounds = renderer.GetOpaqueBoundsInPixels(1.0f, 96.0f, 150.0f);

Assert.AreEqual(163, bounds.Width);
Assert.AreEqual(29, bounds.Height);
```

### See Also

* class [NodeRendererBase](../)
* namespace [Aspose.Words.Rendering](../../../aspose.words.rendering/)
* assembly [Aspose.Words](../../../)
