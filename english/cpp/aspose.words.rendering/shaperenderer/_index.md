---
title: Aspose::Words::Rendering::ShapeRenderer class
linktitle: ShapeRenderer
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Rendering::ShapeRenderer class. Provides methods to render an individual Shape or GroupShape to a raster or vector image or to a Graphics object. To learn more, visit the  documentation article in C++.'
type: docs
weight: 4000
url: /cpp/aspose.words.rendering/shaperenderer/
---
## ShapeRenderer class


Provides methods to render an individual [Shape](../../aspose.words.drawing/shape/) or [GroupShape](../../aspose.words.drawing/groupshape/) to a raster or vector image or to a Graphics object. To learn more, visit the [Working with Shapes](https://docs.aspose.com/words/cpp/working-with-shapes/) documentation article.

```cpp
class ShapeRenderer : public Aspose::Words::Rendering::NodeRendererBase
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
| [RenderToScale](../noderendererbase/rendertoscale/)(const System::SharedPtr\<System::Drawing::Graphics\>\&, float, float, float) | Renders the shape into a **Graphics** object to a specified scale. |
| [RenderToSize](../noderendererbase/rendertosize/)(const System::SharedPtr\<System::Drawing::Graphics\>\&, float, float, float, float) | Renders the shape into a **Graphics** object to a specified size. |
| [Save](../noderendererbase/save/)(const System::String\&, System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>) | Renders the shape into an image and saves into a file. |
| [Save](../noderendererbase/save/)(const System::String\&, System::SharedPtr\<Aspose::Words::Saving::SvgSaveOptions\>) | Renders the shape into an SVG image and saves into a file. |
| [Save](../noderendererbase/save/)(const System::SharedPtr\<System::IO::Stream\>\&, System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>) | Renders the shape into an image and saves into a stream. |
| [Save](../noderendererbase/save/)(const System::SharedPtr\<System::IO::Stream\>\&, System::SharedPtr\<Aspose::Words::Saving::SvgSaveOptions\>) | Renders the shape into an SVG image and saves into a stream. |
| [Save](../noderendererbase/save/)(std::basic_ostream\<CharType, Traits\>\&, System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>) |  |
| [Save](../noderendererbase/save/)(std::basic_ostream\<CharType, Traits\>\&, System::SharedPtr\<Aspose::Words::Saving::SvgSaveOptions\>) |  |
| [ShapeRenderer](./shaperenderer/)(const System::SharedPtr\<Aspose::Words::Drawing::ShapeBase\>\&) | Initializes a new instance of this class. |
| static [Type](./type/)() |  |
## See Also

* Class [NodeRendererBase](../noderendererbase/)
* Namespace [Aspose::Words::Rendering](../)
* Library [Aspose.Words for C++](../../)
