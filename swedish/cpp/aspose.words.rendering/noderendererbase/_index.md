---
title: "Aspose::Words::Rendering::NodeRendererBase class"
linktitle: "NodeRendererBase"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Rendering::NodeRendererBase class. Bas-klass för ShapeRenderer och OfficeMathRenderer. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 1000
url: /sv/cpp/aspose.words.rendering/noderendererbase/
---
## NodeRendererBase class


Bas-klass för [ShapeRenderer](../shaperenderer/) och [OfficeMathRenderer](../officemathrenderer/). För att lära dig mer, besök dokumentationsartikeln [Arbeta med former](https://docs.aspose.com/words/cpp/working-with-shapes/).

```cpp
class NodeRendererBase : public System::Object
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [get_BoundsInPoints](./get_boundsinpoints/)() const | Hämtar de faktiska gränserna för formen i punkter. |
| [get_OpaqueBoundsInPoints](./get_opaqueboundsinpoints/)() | Hämtar de ogenomskinliga gränserna för formen i punkter. |
| [get_SizeInPoints](./get_sizeinpoints/)() | Hämtar den faktiska storleken på formen i punkter. |
| [GetBoundsInPixels](./getboundsinpixels/)(float, float) | Beräknar formens gränser i pixlar för en angiven zoomfaktor och upplösning. |
| [GetBoundsInPixels](./getboundsinpixels/)(float, float, float) | Beräknar formens gränser i pixlar för en angiven zoomfaktor och upplösning. |
| [GetOpaqueBoundsInPixels](./getopaqueboundsinpixels/)(float, float) | Beräknar de ogenomskinliga gränserna för formen i pixlar för en angiven zoomfaktor och upplösning. |
| [GetOpaqueBoundsInPixels](./getopaqueboundsinpixels/)(float, float, float) | Beräknar de ogenomskinliga gränserna för formen i pixlar för en angiven zoomfaktor och upplösning. |
| [GetSizeInPixels](./getsizeinpixels/)(float, float) | Beräknar formens storlek i pixlar för en angiven zoomfaktor och upplösning. |
| [GetSizeInPixels](./getsizeinpixels/)(float, float, float) | Beräknar formens storlek i pixlar för en angiven zoomfaktor och upplösning. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [NodeRendererBase](./noderendererbase/)() |  |
| [RenderToScale](./rendertoscale/)(const System::SharedPtr\<System::Drawing::Graphics\>\&, float, float, float) | Renderar formen till ett **Graphics**-objekt med en angiven skala. |
| [RenderToSize](./rendertosize/)(const System::SharedPtr\<System::Drawing::Graphics\>\&, float, float, float, float) | Renderar formen till ett **Graphics**-objekt med en angiven storlek. |
| [Save](./save/)(const System::String\&, System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>) | Renderar formen till en bild och sparar den i en fil. |
| [Save](./save/)(const System::String\&, System::SharedPtr\<Aspose::Words::Saving::SvgSaveOptions\>) | Renderar formen till en SVG-bild och sparar den i en fil. |
| [Save](./save/)(const System::SharedPtr\<System::IO::Stream\>\&, System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>) | Renderar formen till en bild och sparar den i en ström. |
| [Save](./save/)(const System::SharedPtr\<System::IO::Stream\>\&, System::SharedPtr\<Aspose::Words::Saving::SvgSaveOptions\>) | Renderar formen till en SVG-bild och sparar den i en ström. |
| [Save](./save/)(std::basic_ostream\<CharType, Traits\>\&, System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>) |  |
| [Save](./save/)(std::basic_ostream\<CharType, Traits\>\&, System::SharedPtr\<Aspose::Words::Saving::SvgSaveOptions\>) |  |
| static [Type](./type/)() |  |

## Exempel



Visar hur man mäter och skalar former.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Office math.docx");

auto officeMath = System::ExplicitCast<Aspose::Words::Math::OfficeMath>(doc->GetChild(Aspose::Words::NodeType::OfficeMath, 0, true));
auto renderer = System::MakeObject<Aspose::Words::Rendering::OfficeMathRenderer>(officeMath);

// Verifiera storleken på bilden som OfficeMath-objektet kommer att skapa när vi renderar det.
ASSERT_NEAR(122.0f, renderer->get_SizeInPoints().get_Width(), 0.25f);
ASSERT_NEAR(13.0f, renderer->get_SizeInPoints().get_Height(), 0.15f);

ASSERT_NEAR(122.0f, renderer->get_BoundsInPoints().get_Width(), 0.25f);
ASSERT_NEAR(13.0f, renderer->get_BoundsInPoints().get_Height(), 0.15f);

// Former med transparenta delar kan innehålla olika värden i egenskaperna "OpaqueBoundsInPoints".
ASSERT_NEAR(119.5f, renderer->get_OpaqueBoundsInPoints().get_Width(), 0.25f);
ASSERT_NEAR(14.2f, renderer->get_OpaqueBoundsInPoints().get_Height(), 0.1f);

// Hämta formens storlek i pixlar, med linjär skalning till ett specifikt DPI.
System::Drawing::Rectangle bounds = renderer->GetBoundsInPixels(1.0f, 96.0f);
System::String dpi96 = u"DPI 96";
ASSERT_EQ(163, bounds.get_Width()) << (dpi96);
ASSERT_EQ(18, bounds.get_Height()) << (dpi96);

// Hämta formens storlek i pixlar, men med ett annat DPI för horisontella och vertikala dimensioner.
bounds = renderer->GetBoundsInPixels(1.0f, 96.0f, 150.0f);
System::String dpi96150 = u"DPI 96 150";
ASSERT_EQ(163, bounds.get_Width()) << (dpi96150);
ASSERT_EQ(27, bounds.get_Height()) << (dpi96150);

// De ogenomskinliga gränserna kan också variera här.
bounds = renderer->GetOpaqueBoundsInPixels(1.0f, 96.0f);
System::String dpi96Opaque = u"DPI 96 Opaque";
ASSERT_EQ(160, bounds.get_Width()) << (dpi96Opaque);
ASSERT_EQ(19, bounds.get_Height()) << (dpi96Opaque);

bounds = renderer->GetOpaqueBoundsInPixels(1.0f, 96.0f, 150.0f);
System::String dpi96150Opaque = u"DPI 96 150 Opaque";
ASSERT_EQ(160, bounds.get_Width()) << (dpi96150Opaque);
ASSERT_EQ(29, bounds.get_Height()) << (dpi96150Opaque);
```

## Se även

* Namespace [Aspose::Words::Rendering](../)
* Library [Aspose.Words for C++](../../)
