---
title: Aspose::Words::Rendering::NodeRendererBase::GetSizeInPixels method
linktitle: GetSizeInPixels
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Rendering::NodeRendererBase::GetSizeInPixels method. Calculates the size of the shape in pixels for a specified zoom factor and resolution in C++.'
type: docs
weight: 8000
url: /cpp/aspose.words.rendering/noderendererbase/getsizeinpixels/
---
## NodeRendererBase::GetSizeInPixels(float, float) method


Calculates the size of the shape in pixels for a specified zoom factor and resolution.

```cpp
System::Drawing::Size Aspose::Words::Rendering::NodeRendererBase::GetSizeInPixels(float scale, float dpi)
```


| Parameter | Type | Description |
| --- | --- | --- |
| scale | float | The zoom factor (1.0 is 100%). |
| dpi | float | The resolution (horizontal and vertical) to convert from points to pixels (dots per inch). |

### ReturnValue

The size of the shape in pixels.
## Remarks


This method converts [SizeInPoints](../get_sizeinpoints/) into size in pixels and it is useful when you want to create a bitmap for rendering the shape neatly onto the bitmap.

## Examples



Shows how to measure and scale shapes. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"Office math.docx");

auto officeMath = System::ExplicitCast<OfficeMath>(doc->GetChild(NodeType::OfficeMath, 0, true));
auto renderer = MakeObject<OfficeMathRenderer>(officeMath);

// Verify the size of the image that the OfficeMath object will create when we render it.
ASSERT_NEAR(120, renderer->get_SizeInPoints().get_Width(), 0.3f);
ASSERT_NEAR(13.0f, renderer->get_SizeInPoints().get_Height(), 0.1f);

ASSERT_NEAR(120, renderer->get_BoundsInPoints().get_Width(), 0.3f);
ASSERT_NEAR(13.0f, renderer->get_BoundsInPoints().get_Height(), 0.1f);

// Shapes with transparent parts may contain different values in the "OpaqueBoundsInPoints" properties.
ASSERT_NEAR(120, renderer->get_OpaqueBoundsInPoints().get_Width(), 0.3f);
ASSERT_NEAR(14.2f, renderer->get_OpaqueBoundsInPoints().get_Height(), 0.1f);

// Get the shape size in pixels, with linear scaling to a specific DPI.
System::Drawing::Rectangle bounds = renderer->GetBoundsInPixels(1.0f, 96.0f);

ASSERT_EQ(160, bounds.get_Width());
ASSERT_EQ(18, bounds.get_Height());

// Get the shape size in pixels, but with a different DPI for the horizontal and vertical dimensions.
bounds = renderer->GetBoundsInPixels(1.0f, 96.0f, 150.0f);
ASSERT_EQ(160, bounds.get_Width());
ASSERT_EQ(28, bounds.get_Height());

// The opaque bounds may vary here also.
bounds = renderer->GetOpaqueBoundsInPixels(1.0f, 96.0f);

ASSERT_EQ(160, bounds.get_Width());
ASSERT_EQ(18, bounds.get_Height());

bounds = renderer->GetOpaqueBoundsInPixels(1.0f, 96.0f, 150.0f);

ASSERT_EQ(160, bounds.get_Width());
ASSERT_EQ(30, bounds.get_Height());
```

## See Also

* Class [NodeRendererBase](../)
* Namespace [Aspose::Words::Rendering](../../)
* Library [Aspose.Words for C++](../../../)
## NodeRendererBase::GetSizeInPixels(float, float, float) method


Calculates the size of the shape in pixels for a specified zoom factor and resolution.

```cpp
System::Drawing::Size Aspose::Words::Rendering::NodeRendererBase::GetSizeInPixels(float scale, float horizontalDpi, float verticalDpi)
```


| Parameter | Type | Description |
| --- | --- | --- |
| scale | float | The zoom factor (1.0 is 100%). |
| horizontalDpi | float | The horizontal resolution to convert from points to pixels (dots per inch). |
| verticalDpi | float | The vertical resolution to convert from points to pixels (dots per inch). |

### ReturnValue

The size of the shape in pixels.
## Remarks


This method converts [SizeInPoints](../get_sizeinpoints/) into size in pixels and it is useful when you want to create a bitmap for rendering the shape neatly onto the bitmap.

## Examples



Shows how to measure and scale shapes. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"Office math.docx");

auto officeMath = System::ExplicitCast<OfficeMath>(doc->GetChild(NodeType::OfficeMath, 0, true));
auto renderer = MakeObject<OfficeMathRenderer>(officeMath);

// Verify the size of the image that the OfficeMath object will create when we render it.
ASSERT_NEAR(120, renderer->get_SizeInPoints().get_Width(), 0.3f);
ASSERT_NEAR(13.0f, renderer->get_SizeInPoints().get_Height(), 0.1f);

ASSERT_NEAR(120, renderer->get_BoundsInPoints().get_Width(), 0.3f);
ASSERT_NEAR(13.0f, renderer->get_BoundsInPoints().get_Height(), 0.1f);

// Shapes with transparent parts may contain different values in the "OpaqueBoundsInPoints" properties.
ASSERT_NEAR(120, renderer->get_OpaqueBoundsInPoints().get_Width(), 0.3f);
ASSERT_NEAR(14.2f, renderer->get_OpaqueBoundsInPoints().get_Height(), 0.1f);

// Get the shape size in pixels, with linear scaling to a specific DPI.
System::Drawing::Rectangle bounds = renderer->GetBoundsInPixels(1.0f, 96.0f);

ASSERT_EQ(160, bounds.get_Width());
ASSERT_EQ(18, bounds.get_Height());

// Get the shape size in pixels, but with a different DPI for the horizontal and vertical dimensions.
bounds = renderer->GetBoundsInPixels(1.0f, 96.0f, 150.0f);
ASSERT_EQ(160, bounds.get_Width());
ASSERT_EQ(28, bounds.get_Height());

// The opaque bounds may vary here also.
bounds = renderer->GetOpaqueBoundsInPixels(1.0f, 96.0f);

ASSERT_EQ(160, bounds.get_Width());
ASSERT_EQ(18, bounds.get_Height());

bounds = renderer->GetOpaqueBoundsInPixels(1.0f, 96.0f, 150.0f);

ASSERT_EQ(160, bounds.get_Width());
ASSERT_EQ(30, bounds.get_Height());
```

## See Also

* Class [NodeRendererBase](../)
* Namespace [Aspose::Words::Rendering](../../)
* Library [Aspose.Words for C++](../../../)
