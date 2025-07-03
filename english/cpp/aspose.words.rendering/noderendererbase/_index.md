---
title: Aspose::Words::Rendering::NodeRendererBase class
linktitle: NodeRendererBase
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Rendering::NodeRendererBase class. Base class for ShapeRenderer and OfficeMathRenderer. To learn more, visit the  documentation article in C++.'
type: docs
weight: 1000
url: /cpp/aspose.words.rendering/noderendererbase/
---
## NodeRendererBase class


Base class for [ShapeRenderer](../shaperenderer/) and [OfficeMathRenderer](../officemathrenderer/). To learn more, visit the [Working with Shapes](https://docs.aspose.com/words/cpp/working-with-shapes/) documentation article.

```cpp
class NodeRendererBase : public System::Object
```

## Methods

| Method | Description |
| --- | --- |
| [get_BoundsInPoints](./get_boundsinpoints/)() const | Gets the actual bounds of the shape in points. |
| [get_OpaqueBoundsInPoints](./get_opaqueboundsinpoints/)() | Gets the opaque bounds of the shape in points. |
| [get_SizeInPoints](./get_sizeinpoints/)() | Gets the actual size of the shape in points. |
| [GetBoundsInPixels](./getboundsinpixels/)(float, float) | Calculates the bounds of the shape in pixels for a specified zoom factor and resolution. |
| [GetBoundsInPixels](./getboundsinpixels/)(float, float, float) | Calculates the bounds of the shape in pixels for a specified zoom factor and resolution. |
| [GetOpaqueBoundsInPixels](./getopaqueboundsinpixels/)(float, float) | Calculates the opaque bounds of the shape in pixels for a specified zoom factor and resolution. |
| [GetOpaqueBoundsInPixels](./getopaqueboundsinpixels/)(float, float, float) | Calculates the opaque bounds of the shape in pixels for a specified zoom factor and resolution. |
| [GetSizeInPixels](./getsizeinpixels/)(float, float) | Calculates the size of the shape in pixels for a specified zoom factor and resolution. |
| [GetSizeInPixels](./getsizeinpixels/)(float, float, float) | Calculates the size of the shape in pixels for a specified zoom factor and resolution. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [NodeRendererBase](./noderendererbase/)() |  |
| [RenderToScale](./rendertoscale/)(const System::SharedPtr\<System::Drawing::Graphics\>\&, float, float, float) | Renders the shape into a **Graphics** object to a specified scale. |
| [RenderToSize](./rendertosize/)(const System::SharedPtr\<System::Drawing::Graphics\>\&, float, float, float, float) | Renders the shape into a **Graphics** object to a specified size. |
| [Save](./save/)(const System::String\&, System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>) | Renders the shape into an image and saves into a file. |
| [Save](./save/)(const System::String\&, System::SharedPtr\<Aspose::Words::Saving::SvgSaveOptions\>) | Renders the shape into an SVG image and saves into a file. |
| [Save](./save/)(const System::SharedPtr\<System::IO::Stream\>\&, System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>) | Renders the shape into an image and saves into a stream. |
| [Save](./save/)(const System::SharedPtr\<System::IO::Stream\>\&, System::SharedPtr\<Aspose::Words::Saving::SvgSaveOptions\>) | Renders the shape into an SVG image and saves into a stream. |
| [Save](./save/)(std::basic_ostream\<CharType, Traits\>\&, System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>) |  |
| [Save](./save/)(std::basic_ostream\<CharType, Traits\>\&, System::SharedPtr\<Aspose::Words::Saving::SvgSaveOptions\>) |  |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words::Rendering](../)
* Library [Aspose.Words for C++](../../)
