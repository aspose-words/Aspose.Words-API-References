---
title: "Aspose::Words::Drawing::Charts::ChartLegend class"
linktitle: "ChartLegend"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Drawing::Charts::ChartLegend class. Representerar diagramlegendans egenskaper. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 11000
url: /sv/cpp/aspose.words.drawing.charts/chartlegend/
---
## ChartLegend class


Representerar diagramförklaringens egenskaper. För att lära dig mer, besök dokumentationsartikeln [Working with Charts](https://docs.aspose.com/words/cpp/working-with-charts/).

```cpp
class ChartLegend : public Aspose::Words::Drawing::Core::Dml::IDmlExtensionListSource,
                    public Aspose::Words::Drawing::Charts::Core::IChartFormatSource
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [get_Font](./get_font/)() | Tillhandahåller åtkomst till standardteckensnittsformatering för legendposter. För att åsidosätta teckensnittsformateringen för en specifik legendpost, använd the[Font](../chartlegendentry/get_font/) egenskapen. |
| [get_Format](./get_format/)() | Tillhandahåller åtkomst till fyllnings- och linjeformatering för legend. |
| [get_LegendEntries](./get_legendentries/)() const | Returnerar en samling av legendposter för alla serier och trendlinjer i föräldradiagrammet. |
| [get_Overlay](./get_overlay/)() const | Bestämmer om andra diagramelement ska tillåtas överlappa legend. Standardvärdet är **false**. |
| [get_Position](./get_position/)() | Anger positionen för legend på ett diagram. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Overlay](./set_overlay/)(bool) | Sättare för [Aspose::Words::Drawing::Charts::ChartLegend::get_Overlay](./get_overlay/). |
| [set_Position](./set_position/)(Aspose::Words::Drawing::Charts::LegendPosition) | Sättare för [Aspose::Words::Drawing::Charts::ChartLegend::get_Position](./get_position/). |
| static [Type](./type/)() |  |

## Exempel



Visar hur man redigerar diagramlegendens utseende.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Line, 450, 300);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();

ASSERT_EQ(3, chart->get_Series()->get_Count());
ASSERT_EQ(u"Series 1", chart->get_Series()->idx_get(0)->get_Name());
ASSERT_EQ(u"Series 2", chart->get_Series()->idx_get(1)->get_Name());
ASSERT_EQ(u"Series 3", chart->get_Series()->idx_get(2)->get_Name());

// Flytta diagramlegendens till övre högra hörnet.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartLegend> legend = chart->get_Legend();
legend->set_Position(Aspose::Words::Drawing::Charts::LegendPosition::TopRight);

// Ge andra diagramelement, såsom grafen, mer utrymme genom att tillåta dem att överlappa legend.
legend->set_Overlay(true);

doc->Save(get_ArtifactsDir() + u"Charts.ChartLegend.docx");
```

## Se även

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
