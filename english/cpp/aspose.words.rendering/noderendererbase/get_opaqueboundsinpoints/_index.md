---
title: Aspose::Words::Rendering::NodeRendererBase::get_OpaqueBoundsInPoints method
linktitle: get_OpaqueBoundsInPoints
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Rendering::NodeRendererBase::get_OpaqueBoundsInPoints method. Gets the opaque bounds of the shape in points in C++.'
type: docs
weight: 4000
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
auto doc = MakeObject<Document>(MyDir + u"Office math.docx");

auto officeMath = System::DynamicCast<OfficeMath>(doc->GetChild(NodeType::OfficeMath, 0, true));
auto renderer = MakeObject<OfficeMathRenderer>(officeMath);

// Verify the size of the image that the OfficeMath object will create when we render it.
ASSERT_NEAR(119.0f, renderer->get_SizeInPoints().get_Width(), 0.2f);
ASSERT_NEAR(13.0f, renderer->get_SizeInPoints().get_Height(), 0.1f);

ASSERT_NEAR(119.0f, renderer->get_BoundsInPoints().get_Width(), 0.2f);
ASSERT_NEAR(13.0f, renderer->get_BoundsInPoints().get_Height(), 0.1f);

// Shapes with transparent parts may contain different values in the "OpaqueBoundsInPoints" properties.
ASSERT_NEAR(119.0f, renderer->get_OpaqueBoundsInPoints().get_Width(), 0.2f);
ASSERT_NEAR(14.2f, renderer->get_OpaqueBoundsInPoints().get_Height(), 0.1f);

// Get the shape size in pixels, with linear scaling to a specific DPI.
System::Drawing::Rectangle bounds = renderer->GetBoundsInPixels(1.0f, 96.0f);

ASSERT_EQ(159, bounds.get_Width());
ASSERT_EQ(18, bounds.get_Height());

// Get the shape size in pixels, but with a different DPI for the horizontal and vertical dimensions.
bounds = renderer->GetBoundsInPixels(1.0f, 96.0f, 150.0f);
ASSERT_EQ(159, bounds.get_Width());
ASSERT_EQ(28, bounds.get_Height());

// The opaque bounds may vary here also.
bounds = renderer->GetOpaqueBoundsInPixels(1.0f, 96.0f);

ASSERT_EQ(159, bounds.get_Width());
ASSERT_EQ(18, bounds.get_Height());

bounds = renderer->GetOpaqueBoundsInPixels(1.0f, 96.0f, 150.0f);

ASSERT_EQ(159, bounds.get_Width());
ASSERT_EQ(30, bounds.get_Height());
```

## See Also

* Class [NodeRendererBase](../)
* Namespace [Aspose::Words::Rendering](../../)
* Library [Aspose.Words for C++](../../../)
