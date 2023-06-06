---
title: Aspose::Words::Rendering::OfficeMathRenderer class
linktitle: OfficeMathRenderer
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Rendering::OfficeMathRenderer class. Provides methods to render an individual OfficeMath to a raster or vector image or to a Graphics object. To learn more, visit the  documentation article in C++.'
type: docs
weight: 2000
url: /cpp/aspose.words.rendering/officemathrenderer/
---
## OfficeMathRenderer class


Provides methods to render an individual [OfficeMath](../../aspose.words.math/officemath/) to a raster or vector image or to a Graphics object. To learn more, visit the [Working with OfficeMath](https://docs.aspose.com/words/cpp/working-with-officemath/) documentation article.

```cpp
class OfficeMathRenderer : public Aspose::Words::Rendering::NodeRendererBase
```

## Methods

| Method | Description |
| --- | --- |
| [get_BoundsInPoints](../noderendererbase/get_boundsinpoints/)() const | Gets the actual bounds of the shape in points. |
| [get_OpaqueBoundsInPoints](../noderendererbase/get_opaqueboundsinpoints/)() | Gets the opaque bounds of the shape in points. |
| [get_SizeInPoints](../noderendererbase/get_sizeinpoints/)() | Gets the actual size of the shape in points. |
| [GetBoundsInPixels](../noderendererbase/getboundsinpixels/)(float, float) | Calculates the bounds of the shape in pixels for a specified zoom factor and resolution. |
| [GetBoundsInPixels](../noderendererbase/getboundsinpixels/)(float, float, float) | Calculates the bounds of the shape in pixels for a specified zoom factor and resolution. |
| [GetOpaqueBoundsInPixels](../noderendererbase/getopaqueboundsinpixels/)(float, float) | Calculates the opaque bounds of the shape in pixels for a specified zoom factor and resolution. |
| [GetOpaqueBoundsInPixels](../noderendererbase/getopaqueboundsinpixels/)(float, float, float) | Calculates the opaque bounds of the shape in pixels for a specified zoom factor and resolution. |
| [GetSizeInPixels](../noderendererbase/getsizeinpixels/)(float, float) | Calculates the size of the shape in pixels for a specified zoom factor and resolution. |
| [GetSizeInPixels](../noderendererbase/getsizeinpixels/)(float, float, float) | Calculates the size of the shape in pixels for a specified zoom factor and resolution. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [NodeRendererBase](../noderendererbase/noderendererbase/)() |  |
| [OfficeMathRenderer](./officemathrenderer/)(const System::SharedPtr\<Aspose::Words::Math::OfficeMath\>\&) | Initializes a new instance of this class. |
| [RenderToScale](../noderendererbase/rendertoscale/)(const System::SharedPtr\<System::Drawing::Graphics\>\&, float, float, float) | Renders the shape into a **Graphics** object to a specified scale. |
| [RenderToSize](../noderendererbase/rendertosize/)(const System::SharedPtr\<System::Drawing::Graphics\>\&, float, float, float, float) | Renders the shape into a **Graphics** object to a specified size. |
| [Save](../noderendererbase/save/)(const System::String\&, System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>) | Renders the shape into an image and saves into a file. |
| [Save](../noderendererbase/save/)(const System::SharedPtr\<System::IO::Stream\>\&, System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>) | Renders the shape into an image and saves into a stream. |
| [Save](../noderendererbase/save/)(std::basic_ostream\<CharType, Traits\>\&, System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>) |  |
| static [Type](./type/)() |  |

## Examples



Shows how to measure and scale shapes. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"Office math.docx");

auto officeMath = System::ExplicitCast<OfficeMath>(doc->GetChild(NodeType::OfficeMath, 0, true));
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

* Class [NodeRendererBase](../noderendererbase/)
* Namespace [Aspose::Words::Rendering](../)
* Library [Aspose.Words for C++](../../)
