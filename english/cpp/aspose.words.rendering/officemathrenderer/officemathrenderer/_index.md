---
title: Aspose::Words::Rendering::OfficeMathRenderer::OfficeMathRenderer constructor
linktitle: OfficeMathRenderer
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Rendering::OfficeMathRenderer::OfficeMathRenderer constructor. Initializes a new instance of this class in C++.'
type: docs
weight: 2000
url: /cpp/aspose.words.rendering/officemathrenderer/officemathrenderer/
---
## OfficeMathRenderer::OfficeMathRenderer constructor


Initializes a new instance of this class.

```cpp
Aspose::Words::Rendering::OfficeMathRenderer::OfficeMathRenderer(const System::SharedPtr<Aspose::Words::Math::OfficeMath> &math)
```


| Parameter | Type | Description |
| --- | --- | --- |
| math | const System::SharedPtr\<Aspose::Words::Math::OfficeMath\>\& | The [OfficeMath](../../../aspose.words.math/officemath/) object that you want to render. |

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

* Class [OfficeMath](../../../aspose.words.math/officemath/)
* Class [OfficeMathRenderer](../)
* Namespace [Aspose::Words::Rendering](../../)
* Library [Aspose.Words for C++](../../../)
