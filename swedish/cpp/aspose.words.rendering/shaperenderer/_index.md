---
title: "Aspose::Words::Rendering::ShapeRenderer class"
linktitle: "ShapeRenderer"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Rendering::ShapeRenderer class. Tillhandahåller metoder för att rendera en enskild Shape eller GroupShape till en raster- eller vektorbild eller till ett Graphics-objekt. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 4000
url: /sv/cpp/aspose.words.rendering/shaperenderer/
---
## ShapeRenderer class


Tillhandahåller metoder för att rendera en enskild [Shape](../../aspose.words.drawing/shape/) eller [GroupShape](../../aspose.words.drawing/groupshape/) till en raster- eller vektorbild eller till ett Graphics-objekt. För att lära dig mer, besök dokumentationsartikeln [Arbeta med former](https://docs.aspose.com/words/cpp/working-with-shapes/).

```cpp
class ShapeRenderer : public Aspose::Words::Rendering::NodeRendererBase
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [get_BoundsInPoints](../noderendererbase/get_boundsinpoints/)() const | Hämtar de faktiska gränserna för formen i punkter. |
| [get_OpaqueBoundsInPoints](../noderendererbase/get_opaqueboundsinpoints/)() | Hämtar de ogenomskinliga gränserna för formen i punkter. |
| [get_SizeInPoints](../noderendererbase/get_sizeinpoints/)() | Hämtar den faktiska storleken på formen i punkter. |
| [GetBoundsInPixels](../noderendererbase/getboundsinpixels/)(float, float) | Beräknar formens gränser i pixlar för en angiven zoomfaktor och upplösning. |
| [GetBoundsInPixels](../noderendererbase/getboundsinpixels/)(float, float, float) | Beräknar formens gränser i pixlar för en angiven zoomfaktor och upplösning. |
| [GetOpaqueBoundsInPixels](../noderendererbase/getopaqueboundsinpixels/)(float, float) | Beräknar de ogenomskinliga gränserna för formen i pixlar för en angiven zoomfaktor och upplösning. |
| [GetOpaqueBoundsInPixels](../noderendererbase/getopaqueboundsinpixels/)(float, float, float) | Beräknar de ogenomskinliga gränserna för formen i pixlar för en angiven zoomfaktor och upplösning. |
| [GetSizeInPixels](../noderendererbase/getsizeinpixels/)(float, float) | Beräknar formens storlek i pixlar för en angiven zoomfaktor och upplösning. |
| [GetSizeInPixels](../noderendererbase/getsizeinpixels/)(float, float, float) | Beräknar formens storlek i pixlar för en angiven zoomfaktor och upplösning. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [NodeRendererBase](../noderendererbase/noderendererbase/)() |  |
| [RenderToScale](../noderendererbase/rendertoscale/)(const System::SharedPtr\<System::Drawing::Graphics\>\&, float, float, float) | Renderar formen till ett **Graphics**-objekt med en angiven skala. |
| [RenderToSize](../noderendererbase/rendertosize/)(const System::SharedPtr\<System::Drawing::Graphics\>\&, float, float, float, float) | Renderar formen till ett **Graphics**-objekt med en angiven storlek. |
| [Save](../noderendererbase/save/)(const System::String\&, System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>) | Renderar formen till en bild och sparar den i en fil. |
| [Save](../noderendererbase/save/)(const System::String\&, System::SharedPtr\<Aspose::Words::Saving::SvgSaveOptions\>) | Renderar formen till en SVG-bild och sparar den i en fil. |
| [Save](../noderendererbase/save/)(const System::SharedPtr\<System::IO::Stream\>\&, System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>) | Renderar formen till en bild och sparar den i en ström. |
| [Save](../noderendererbase/save/)(const System::SharedPtr\<System::IO::Stream\>\&, System::SharedPtr\<Aspose::Words::Saving::SvgSaveOptions\>) | Renderar formen till en SVG-bild och sparar den i en ström. |
| [Save](../noderendererbase/save/)(std::basic_ostream\<CharType, Traits\>\&, System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>) |  |
| [Save](../noderendererbase/save/)(std::basic_ostream\<CharType, Traits\>\&, System::SharedPtr\<Aspose::Words::Saving::SvgSaveOptions\>) |  |
| [ShapeRenderer](./shaperenderer/)(const System::SharedPtr\<Aspose::Words::Drawing::ShapeBase\>\&) | Initierar en ny instans av den här klassen. |
| static [Type](./type/)() |  |
## Se även

* Class [NodeRendererBase](../noderendererbase/)
* Namespace [Aspose::Words::Rendering](../)
* Library [Aspose.Words for C++](../../)
