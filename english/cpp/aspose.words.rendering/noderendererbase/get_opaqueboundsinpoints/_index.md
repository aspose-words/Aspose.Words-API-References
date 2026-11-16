---
title: Aspose::Words::Rendering::NodeRendererBase::get_OpaqueBoundsInPoints method
linktitle: get_OpaqueBoundsInPoints
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Rendering::NodeRendererBase::get_OpaqueBoundsInPoints method. Gets the opaque bounds of the shape in points in C++.'
type: docs
weight: 15000
url: /cpp/aspose.words.rendering/noderendererbase/get_opaqueboundsinpoints/
---
## NodeRendererBase::get_OpaqueBoundsInPoints method


Gets the opaque bounds of the shape in points.

```cpp
System::Drawing::RectangleF Aspose::Words::Rendering::NodeRendererBase::get_OpaqueBoundsInPoints()
```

## Remarks


This property returns the opaque (i.e. transparent parts of the shape are ignored) bounding box of the shape. The bounds takes the shape rotation into account.
## Examples


Shows how to measure and scale shapes.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(System::String(get_MyDir() + u"Office math.docx"));

auto officeMath = System::ExplicitCast<Aspose::Words::Math::OfficeMath>(doc->GetChild(NodeType::OfficeMath, 0, true));
auto renderer = System::MakeObject<Aspose::Words::Rendering::OfficeMathRenderer>(officeMath);

// Verify the size of the image that the OfficeMath object will create when we render it.
ASSERT_NEAR(renderer->get_SizeInPoints().get_Width(), 122.0f, 0.25f);
ASSERT_NEAR(renderer->get_SizeInPoints().get_Height(), 13.0f, 0.15f);

ASSERT_NEAR(renderer->get_BoundsInPoints().get_Width(), 122.0f, 0.25f);
ASSERT_NEAR(renderer->get_BoundsInPoints().get_Height(), 13.0f, 0.15f);

// Shapes with transparent parts may contain different values in the "OpaqueBoundsInPoints" properties.
ASSERT_NEAR(renderer->get_OpaqueBoundsInPoints().get_Width(), 119.5f, 0.25f);
ASSERT_NEAR(renderer->get_OpaqueBoundsInPoints().get_Height(), 14.2f, 0.1f);

// Get the shape size in pixels, with linear scaling to a specific DPI.
System::Drawing::Rectangle bounds = renderer->GetBoundsInPixels(1.0f, 96.0f);
System::String dpi96 = u"DPI 96";
ASSERT_EQ(bounds.get_Width(), 163) << (dpi96);
ASSERT_EQ(bounds.get_Height(), 18) << (dpi96);

// Get the shape size in pixels, but with a different DPI for the horizontal and vertical dimensions.
bounds = renderer->GetBoundsInPixels(1.0f, 96.0f, 150.0f);
System::String dpi96150 = u"DPI 96 150";
ASSERT_EQ(bounds.get_Width(), 163) << (dpi96150);
ASSERT_EQ(bounds.get_Height(), 27) << (dpi96150);

// The opaque bounds may vary here also.
bounds = renderer->GetOpaqueBoundsInPixels(1.0f, 96.0f);
System::String dpi96Opaque = u"DPI 96 Opaque";
ASSERT_EQ(bounds.get_Width(), 160) << (dpi96Opaque);
ASSERT_EQ(bounds.get_Height(), 19) << (dpi96Opaque);

bounds = renderer->GetOpaqueBoundsInPixels(1.0f, 96.0f, 150.0f);
System::String dpi96150Opaque = u"DPI 96 150 Opaque";
ASSERT_EQ(bounds.get_Width(), 160) << (dpi96150Opaque);
ASSERT_EQ(bounds.get_Height(), 29) << (dpi96150Opaque);
```
## See Also

* Class [NodeRendererBase](../)
* Namespace [Aspose::Words::Rendering](../../)
* Library [Aspose.Words for C++](../../../)
