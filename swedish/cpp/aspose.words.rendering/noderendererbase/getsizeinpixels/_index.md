---
title: "Aspose::Words::Rendering::NodeRendererBase::GetSizeInPixels method"
linktitle: "GetSizeInPixels"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Rendering::NodeRendererBase::GetSizeInPixels method. Beräknar storleken på formen i pixlar för en specificerad zoomfaktor och upplösning i C++."
type: docs
weight: 8000
url: /sv/cpp/aspose.words.rendering/noderendererbase/getsizeinpixels/
---
## NodeRendererBase::GetSizeInPixels(float, float) method


Beräknar formens storlek i pixlar för en angiven zoomfaktor och upplösning.

```cpp
System::Drawing::Size Aspose::Words::Rendering::NodeRendererBase::GetSizeInPixels(float scale, float dpi)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| skala | float | Zoomfaktorn (1,0 är 100 %). |
| dpi | float | Upplösningen (horisontell och vertikal) för att konvertera från punkter till pixlar (punkter per tum). |

### ReturnValue

Storleken på formen i pixlar.
## Anmärkningar


Denna metod konverterar [SizeInPoints](../get_sizeinpoints/) till storlek i pixlar och den är användbar när du vill skapa en bitmap för att rendera formen snyggt på bitmapen.

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

* Class [NodeRendererBase](../)
* Namespace [Aspose::Words::Rendering](../../)
* Library [Aspose.Words for C++](../../../)
## NodeRendererBase::GetSizeInPixels(float, float, float) method


Beräknar formens storlek i pixlar för en angiven zoomfaktor och upplösning.

```cpp
System::Drawing::Size Aspose::Words::Rendering::NodeRendererBase::GetSizeInPixels(float scale, float horizontalDpi, float verticalDpi)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| skala | float | Zoomfaktorn (1,0 är 100 %). |
| horizontalDpi | float | Den horisontella upplösningen för att konvertera från punkter till pixlar (punkter per tum). |
| verticalDpi | float | Den vertikala upplösningen för att konvertera från punkter till pixlar (punkter per tum). |

### ReturnValue

Storleken på formen i pixlar.
## Anmärkningar


Denna metod konverterar [SizeInPoints](../get_sizeinpoints/) till storlek i pixlar och den är användbar när du vill skapa en bitmap för att rendera formen snyggt på bitmapen.

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

* Class [NodeRendererBase](../)
* Namespace [Aspose::Words::Rendering](../../)
* Library [Aspose.Words for C++](../../../)
