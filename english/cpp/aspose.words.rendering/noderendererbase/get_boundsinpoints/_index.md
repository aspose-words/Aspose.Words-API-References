---
title: Aspose::Words::Rendering::NodeRendererBase::get_BoundsInPoints method
linktitle: get_BoundsInPoints
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Rendering::NodeRendererBase::get_BoundsInPoints method. Gets the actual bounds of the shape in points in C++.'
type: docs
weight: 3000
url: /cpp/aspose.words.rendering/noderendererbase/get_boundsinpoints/
---
## NodeRendererBase::get_BoundsInPoints method


Gets the actual bounds of the shape in points.

```cpp
System::Drawing::RectangleF Aspose::Words::Rendering::NodeRendererBase::get_BoundsInPoints() const
```

## Remarks


This property returns the actual (as rendered on the page) bounding box of the shape. The bounds takes into account shape rotation (if any).

## Examples



Shows how to measure and scale shapes. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Office math.docx");

auto officeMath = System::ExplicitCast<Aspose::Words::Math::OfficeMath>(doc->GetChild(Aspose::Words::NodeType::OfficeMath, 0, true));
auto renderer = System::MakeObject<Aspose::Words::Rendering::OfficeMathRenderer>(officeMath);

// Verify the size of the image that the OfficeMath object will create when we render it.
ASSERT_NEAR(122.0f, renderer->get_SizeInPoints().get_Width(), 0.25f);
ASSERT_NEAR(13.0f, renderer->get_SizeInPoints().get_Height(), 0.15f);

ASSERT_NEAR(122.0f, renderer->get_BoundsInPoints().get_Width(), 0.25f);
ASSERT_NEAR(13.0f, renderer->get_BoundsInPoints().get_Height(), 0.15f);

// Shapes with transparent parts may contain different values in the "OpaqueBoundsInPoints" properties.
ASSERT_NEAR(122.0f, renderer->get_OpaqueBoundsInPoints().get_Width(), 0.25f);
ASSERT_NEAR(14.2f, renderer->get_OpaqueBoundsInPoints().get_Height(), 0.1f);

// Get the shape size in pixels, with linear scaling to a specific DPI.
System::Drawing::Rectangle bounds = renderer->GetBoundsInPixels(1.0f, 96.0f);

ASSERT_EQ(163, bounds.get_Width());
ASSERT_EQ(18, bounds.get_Height());

// Get the shape size in pixels, but with a different DPI for the horizontal and vertical dimensions.
bounds = renderer->GetBoundsInPixels(1.0f, 96.0f, 150.0f);
ASSERT_EQ(163, bounds.get_Width());
ASSERT_EQ(27, bounds.get_Height());

// The opaque bounds may vary here also.
bounds = renderer->GetOpaqueBoundsInPixels(1.0f, 96.0f);

ASSERT_EQ(163, bounds.get_Width());
ASSERT_EQ(19, bounds.get_Height());

bounds = renderer->GetOpaqueBoundsInPixels(1.0f, 96.0f, 150.0f);

ASSERT_EQ(163, bounds.get_Width());
ASSERT_EQ(29, bounds.get_Height());
```

## See Also

* Class [NodeRendererBase](../)
* Namespace [Aspose::Words::Rendering](../../)
* Library [Aspose.Words for C++](../../../)
