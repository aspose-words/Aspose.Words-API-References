---
title: "Aspose::Words::Drawing::Charts::ChartTitle klass"
linktitle: "ChartTitle"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Drawing::Charts::ChartTitle klass. Tillhandahåller åtkomst till diagramtitelns egenskaper. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 18000
url: /sv/cpp/aspose.words.drawing.charts/charttitle/
---
## ChartTitle class


Ger åtkomst till egenskaperna för diagramrubriken. För att lära dig mer, besök dokumentationsartikeln [Working with Charts](https://docs.aspose.com/words/cpp/working-with-charts/).

```cpp
class ChartTitle : public System::Object
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [get_Font](./get_font/)() | Tillhandahåller åtkomst till teckensnittsformateringen för diagramtiteln. |
| [get_Format](./get_format/)() | Tillhandahåller åtkomst till fyllnings- och linjeformatering för diagramtiteln. |
| [get_Orientation](./get_orientation/)() | Hämtar eller anger orienteringen av diagramtitelns text. |
| [get_Overlay](./get_overlay/)() | Bestämmer om andra diagramelement får överlappa titeln. Som standard är överlagring **false**. |
| [get_Rotation](./get_rotation/)() | Hämtar eller anger rotationen av diagramtiteln i grader. |
| [get_Show](./get_show/)() | Bestämmer om titeln ska visas för detta diagram. Standardvärdet är **true**. |
| [get_Text](./get_text/)() | Hämtar eller anger texten för diagramtiteln. Om **null** eller ett tomt värde anges, visas en automatiskt genererad titel. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Orientation](./set_orientation/)(Aspose::Words::Drawing::ShapeTextOrientation) | Sättare för [Aspose::Words::Drawing::Charts::ChartTitle::get_Orientation](./get_orientation/). |
| [set_Overlay](./set_overlay/)(bool) | Sättare för [Aspose::Words::Drawing::Charts::ChartTitle::get_Overlay](./get_overlay/). |
| [set_Rotation](./set_rotation/)(int32_t) | Sättare för [Aspose::Words::Drawing::Charts::ChartTitle::get_Rotation](./get_rotation/). |
| [set_Show](./set_show/)(bool) | Sättare för [Aspose::Words::Drawing::Charts::ChartTitle::get_Show](./get_show/). |
| [set_Text](./set_text/)(const System::String\&) | Sättare för [Aspose::Words::Drawing::Charts::ChartTitle::get_Text](./get_text/). |
| static [Type](./type/)() |  |

## Exempel



Visar hur man infogar ett diagram och anger en titel.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Infoga en diagramform med en dokumentbyggare och hämta dess diagram.
System::SharedPtr<Aspose::Words::Drawing::Shape> chartShape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Bar, 400, 300);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = chartShape->get_Chart();

// Använd egenskapen "Title" för att ge vårt diagram en titel, som visas i diagramområdets övre centrum.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartTitle> title = chart->get_Title();
title->set_Text(u"My Chart");
title->get_Font()->set_Size(15);
title->get_Font()->set_Color(System::Drawing::Color::get_Blue());

// Ställ in egenskapen "Show" till "true" för att göra titeln synlig.
title->set_Show(true);

// Ställ in egenskapen "Overlay" till "true" för att ge andra diagramelement mer utrymme genom att låta dem överlappa titeln.
title->set_Overlay(true);

doc->Save(get_ArtifactsDir() + u"Charts.ChartTitle.docx");
```

## Se även

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
