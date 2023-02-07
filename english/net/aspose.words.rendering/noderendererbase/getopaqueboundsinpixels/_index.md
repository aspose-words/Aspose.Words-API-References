---
title: NodeRendererBase.GetOpaqueBoundsInPixels
second_title: Aspose.Words for .NET API Reference
description: NodeRendererBase method. Calculates the opaque bounds of the shape in pixels for a specified zoom factor and resolution in C#
type: docs
weight: 50
url: /net/aspose.words.rendering/noderendererbase/getopaqueboundsinpixels/
---
## GetOpaqueBoundsInPixels(float, float) {#getopaqueboundsinpixels}

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
Assert.AreEqual(119.0f, renderer.SizeInPoints.Width, 0.2f);
Assert.AreEqual(13.0f, renderer.SizeInPoints.Height, 0.1f);

Assert.AreEqual(119.0f, renderer.BoundsInPoints.Width, 0.2f);
Assert.AreEqual(13.0f, renderer.BoundsInPoints.Height, 0.1f);

// Shapes with transparent parts may contain different values in the "OpaqueBoundsInPoints" properties.
Assert.AreEqual(119.0f, renderer.OpaqueBoundsInPoints.Width, 0.2f);
Assert.AreEqual(14.2f, renderer.OpaqueBoundsInPoints.Height, 0.1f);

// Get the shape size in pixels, with linear scaling to a specific DPI.
Rectangle bounds = renderer.GetBoundsInPixels(1.0f, 96.0f);

Assert.AreEqual(159, bounds.Width);
Assert.AreEqual(18, bounds.Height);

// Get the shape size in pixels, but with a different DPI for the horizontal and vertical dimensions.
bounds = renderer.GetBoundsInPixels(1.0f, 96.0f, 150.0f);
Assert.AreEqual(159, bounds.Width);
Assert.AreEqual(28, bounds.Height);

// The opaque bounds may vary here also.
bounds = renderer.GetOpaqueBoundsInPixels(1.0f, 96.0f);

Assert.AreEqual(159, bounds.Width);
Assert.AreEqual(18, bounds.Height);

bounds = renderer.GetOpaqueBoundsInPixels(1.0f, 96.0f, 150.0f);

Assert.AreEqual(159, bounds.Width);
Assert.AreEqual(30, bounds.Height);
```

### See Also

* class [NodeRendererBase](../)
* namespace [Aspose.Words.Rendering](../../noderendererbase/)
* assembly [Aspose.Words](../../../)

---

## GetOpaqueBoundsInPixels(float, float, float) {#getopaqueboundsinpixels_1}

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
Assert.AreEqual(119.0f, renderer.SizeInPoints.Width, 0.2f);
Assert.AreEqual(13.0f, renderer.SizeInPoints.Height, 0.1f);

Assert.AreEqual(119.0f, renderer.BoundsInPoints.Width, 0.2f);
Assert.AreEqual(13.0f, renderer.BoundsInPoints.Height, 0.1f);

// Shapes with transparent parts may contain different values in the "OpaqueBoundsInPoints" properties.
Assert.AreEqual(119.0f, renderer.OpaqueBoundsInPoints.Width, 0.2f);
Assert.AreEqual(14.2f, renderer.OpaqueBoundsInPoints.Height, 0.1f);

// Get the shape size in pixels, with linear scaling to a specific DPI.
Rectangle bounds = renderer.GetBoundsInPixels(1.0f, 96.0f);

Assert.AreEqual(159, bounds.Width);
Assert.AreEqual(18, bounds.Height);

// Get the shape size in pixels, but with a different DPI for the horizontal and vertical dimensions.
bounds = renderer.GetBoundsInPixels(1.0f, 96.0f, 150.0f);
Assert.AreEqual(159, bounds.Width);
Assert.AreEqual(28, bounds.Height);

// The opaque bounds may vary here also.
bounds = renderer.GetOpaqueBoundsInPixels(1.0f, 96.0f);

Assert.AreEqual(159, bounds.Width);
Assert.AreEqual(18, bounds.Height);

bounds = renderer.GetOpaqueBoundsInPixels(1.0f, 96.0f, 150.0f);

Assert.AreEqual(159, bounds.Width);
Assert.AreEqual(30, bounds.Height);
```

### See Also

* class [NodeRendererBase](../)
* namespace [Aspose.Words.Rendering](../../noderendererbase/)
* assembly [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
