---
title: NodeRendererBase.SizeInPoints
linktitle: SizeInPoints
articleTitle: SizeInPoints
second_title: Aspose.Words for .NET
description: Discover the NodeRendererBase SizeInPoints property to easily access the precise shape size in points, enhancing your design precision and efficiency.
type: docs
weight: 30
url: /net/aspose.words.rendering/noderendererbase/sizeinpoints/
---
## NodeRendererBase.SizeInPoints property

Gets the actual size of the shape in points.

```csharp
public SizeF SizeInPoints { get; }
```

## Remarks

This property returns the size of the actual (as rendered on the page) bounding box of the shape. The size takes into account shape rotation (if any).

## Examples

Shows how to measure and scale shapes.

```csharp
Document doc = new Document(MyDir + "Office math.docx");

OfficeMath officeMath = (OfficeMath)doc.GetChild(NodeType.OfficeMath, 0, true);
OfficeMathRenderer renderer = new OfficeMathRenderer(officeMath);

// Verify the size of the image that the OfficeMath object will create when we render it.
Assert.That(renderer.SizeInPoints.Width, Is.EqualTo(122.0f).Within(0.25f));
Assert.That(renderer.SizeInPoints.Height, Is.EqualTo(13.0f).Within(0.15f));

Assert.That(renderer.BoundsInPoints.Width, Is.EqualTo(122.0f).Within(0.25f));
Assert.That(renderer.BoundsInPoints.Height, Is.EqualTo(13.0f).Within(0.15f));

// Shapes with transparent parts may contain different values in the "OpaqueBoundsInPoints" properties.
Assert.That(renderer.OpaqueBoundsInPoints.Width, Is.EqualTo(119.5f).Within(0.25f));
Assert.That(renderer.OpaqueBoundsInPoints.Height, Is.EqualTo(14.2f).Within(0.1f));

// Get the shape size in pixels, with linear scaling to a specific DPI.
Rectangle bounds = renderer.GetBoundsInPixels(1.0f, 96.0f);
string dpi96 = "DPI 96";
Assert.That(bounds.Width, Is.EqualTo(163), dpi96);
Assert.That(bounds.Height, Is.EqualTo(18), dpi96);

// Get the shape size in pixels, but with a different DPI for the horizontal and vertical dimensions.
bounds = renderer.GetBoundsInPixels(1.0f, 96.0f, 150.0f);
string dpi96150 = "DPI 96 150";
Assert.That(bounds.Width, Is.EqualTo(163), dpi96150);
Assert.That(bounds.Height, Is.EqualTo(27), dpi96150);

// The opaque bounds may vary here also.
bounds = renderer.GetOpaqueBoundsInPixels(1.0f, 96.0f);
string dpi96Opaque = "DPI 96 Opaque";
Assert.That(bounds.Width, Is.EqualTo(160), dpi96Opaque);
Assert.That(bounds.Height, Is.EqualTo(19), dpi96Opaque);

bounds = renderer.GetOpaqueBoundsInPixels(1.0f, 96.0f, 150.0f);
string dpi96150Opaque = "DPI 96 150 Opaque";
Assert.That(bounds.Width, Is.EqualTo(160), dpi96150Opaque);
Assert.That(bounds.Height, Is.EqualTo(29), dpi96150Opaque);
```

### See Also

* class [NodeRendererBase](../)
* namespace [Aspose.Words.Rendering](../../../aspose.words.rendering/)
* assembly [Aspose.Words](../../../)
