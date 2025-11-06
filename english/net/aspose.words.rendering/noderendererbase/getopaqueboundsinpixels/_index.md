---
title: NodeRendererBase.GetOpaqueBoundsInPixels
linktitle: GetOpaqueBoundsInPixels
articleTitle: GetOpaqueBoundsInPixels
second_title: Aspose.Words for .NET
description: Discover how the NodeRendererBase GetOpaqueBoundsInPixels method efficiently calculates shape bounds in pixels, optimizing for zoom and resolution.
type: docs
weight: 50
url: /net/aspose.words.rendering/noderendererbase/getopaqueboundsinpixels/
---
## GetOpaqueBoundsInPixels(*float, float*) {#getopaqueboundsinpixels}

Calculates the opaque bounds of the shape in pixels for a specified zoom factor and resolution.

```csharp
public Rectangle GetOpaqueBoundsInPixels(float scale, float dpi)
```

| Parameter | Type | Description |
| --- | --- | --- |
| scale | Single | The zoom factor (1.0 is 100%). |
| dpi | Single | The resolution to convert from points to pixels (dots per inch). |

### Return Value

The opaque rectangle of the shape in pixels.

## Remarks

This method converts [`OpaqueBoundsInPoints`](../opaqueboundsinpoints/) into rectangle in pixels and it is useful when you want to create a bitmap for rendering the shape with only opaque part of the shape.

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

---

## GetOpaqueBoundsInPixels(*float, float, float*) {#getopaqueboundsinpixels_1}

Calculates the opaque bounds of the shape in pixels for a specified zoom factor and resolution.

```csharp
public Rectangle GetOpaqueBoundsInPixels(float scale, float horizontalDpi, float verticalDpi)
```

| Parameter | Type | Description |
| --- | --- | --- |
| scale | Single | The zoom factor (1.0 is 100%). |
| horizontalDpi | Single | The horizontal resolution to convert from points to pixels (dots per inch). |
| verticalDpi | Single | The vertical resolution to convert from points to pixels (dots per inch). |

### Return Value

The opaque rectangle of the shape in pixels.

## Remarks

This method converts [`OpaqueBoundsInPoints`](../opaqueboundsinpoints/) into rectangle in pixels and it is useful when you want to create a bitmap for rendering the shape with only opaque part of the shape.

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
