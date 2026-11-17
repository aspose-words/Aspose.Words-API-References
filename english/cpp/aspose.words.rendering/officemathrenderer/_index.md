---
title: Aspose::Words::Rendering::OfficeMathRenderer class
linktitle: OfficeMathRenderer
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Rendering::OfficeMathRenderer class. Provides methods to render an individual OfficeMath to a raster or vector image or to a Graphics object. To learn more, visit the Working with OfficeMath documentation article in C++.'
type: docs
weight: 2000
url: /cpp/aspose.words.rendering/officemathrenderer/
---
## OfficeMathRenderer class


Provides methods to render an individual [OfficeMath](../../aspose.words.math/officemath/) to a raster or vector image or to a Graphics object. 
To learn more, visit the [Working with OfficeMath](https://docs.aspose.com/words/cpp/working-with-officemath/) documentation article.

```cpp
class OfficeMathRenderer : public NodeRendererBase
```

## Methods

| Method | Description |
| --- | --- |
| [OfficeMathRenderer](./officemathrenderer/)(const System::SharedPtr\<Aspose::Words::Math::OfficeMath\> \&) | Initializes a new instance of this class. |
| [GetBoundsInPixels](../noderendererbase/getboundsinpixels/)(float, float) | Calculates the bounds of the shape in pixels for a specified zoom factor and resolution. |
| [GetBoundsInPixels](../noderendererbase/getboundsinpixels/)(float, float, float) | Calculates the bounds of the shape in pixels for a specified zoom factor and resolution. |
| [GetOpaqueBoundsInPixels](../noderendererbase/getopaqueboundsinpixels/)(float, float) | Calculates the opaque bounds of the shape in pixels for a specified zoom factor and resolution. |
| [GetOpaqueBoundsInPixels](../noderendererbase/getopaqueboundsinpixels/)(float, float, float) | Calculates the opaque bounds of the shape in pixels for a specified zoom factor and resolution. |
| [GetSizeInPixels](../noderendererbase/getsizeinpixels/)(float, float) | Calculates the size of the shape in pixels for a specified zoom factor and resolution. |
| [GetSizeInPixels](../noderendererbase/getsizeinpixels/)(float, float, float) | Calculates the size of the shape in pixels for a specified zoom factor and resolution. |
| [RenderToScale](../noderendererbase/rendertoscale/)(const System::SharedPtr\<System::Drawing::Graphics\> \&, float, float, float) | Renders the shape into a Graphics object to a specified scale. |
| [RenderToSize](../noderendererbase/rendertosize/)(const System::SharedPtr\<System::Drawing::Graphics\> \&, float, float, float, float) | Renders the shape into a Graphics object to a specified size. |
| [Save](../noderendererbase/save/)(const System::SharedPtr\<System::IO::Stream\> \&, System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>) | Renders the shape into an image and saves into a stream. |
| [Save](../noderendererbase/save/)(const System::SharedPtr\<System::IO::Stream\> \&, System::SharedPtr\<Aspose::Words::Saving::SvgSaveOptions\>) | Renders the shape into an SVG image and saves into a stream. |
| [Save](../noderendererbase/save/)(const System::String \&, System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>) | Renders the shape into an image and saves into a file. |
| [Save](../noderendererbase/save/)(const System::String \&, System::SharedPtr\<Aspose::Words::Saving::SvgSaveOptions\>) | Renders the shape into an SVG image and saves into a file. |
| [Save](../noderendererbase/save/)(std::basic_ostream\<CharType, Traits\> \&, System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>) | Renders the shape into an image and saves into a stream. |
| [Save](../noderendererbase/save/)(std::basic_ostream\<CharType, Traits\> \&, System::SharedPtr\<Aspose::Words::Saving::SvgSaveOptions\>) | Renders the shape into an SVG image and saves into a stream. |
| [get_BoundsInPoints](../noderendererbase/get_boundsinpoints/)() const | Gets the actual bounds of the shape in points. |
| [get_OpaqueBoundsInPoints](../noderendererbase/get_opaqueboundsinpoints/)() | Gets the opaque bounds of the shape in points. |
| [get_SizeInPoints](../noderendererbase/get_sizeinpoints/)() | Gets the actual size of the shape in points. |
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

* Class [NodeRendererBase](../noderendererbase/)
* Namespace [Aspose::Words::Rendering](../)
* Library [Aspose.Words for C++](../../)
