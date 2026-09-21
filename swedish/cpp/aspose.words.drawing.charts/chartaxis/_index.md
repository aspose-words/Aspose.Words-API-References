---
title: "Aspose::Words::Drawing::Charts::ChartAxis class"
linktitle: "ChartAxis"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Drawing::Charts::ChartAxis-klass. Representerar axelalternativen för diagrammet. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 5000
url: /sv/cpp/aspose.words.drawing.charts/chartaxis/
---
## ChartAxis class


Representerar diagrammets axelalternativ. För att lära dig mer, besök dokumentationsartikeln [Working with Charts](https://docs.aspose.com/words/cpp/working-with-charts/).

```cpp
class ChartAxis : public Aspose::Words::Drawing::Charts::Core::IDmlChartTitleHolder,
                  public Aspose::Words::Drawing::Core::Dml::IDmlExtensionListSource,
                  public Aspose::Words::Drawing::Charts::Core::INumberFormatProvider,
                  public Aspose::Words::Drawing::Charts::Core::IChartFormatSource
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [get_AxisBetweenCategories](./get_axisbetweencategories/)() | Hämtar eller anger en flagga som indikerar om värdeaxeln korsar kategoriaxeln mellan kategorier. |
| [get_BaseTimeUnit](./get_basetimeunit/)() | Returnerar eller anger den minsta tidsenheten som representeras på tidskategori-axeln. |
| [get_CategoryType](./get_categorytype/)() | Hämtar eller anger typen av kategoriaxeln. |
| [get_Crosses](./get_crosses/)() | Anger hur denna axel korsar den vinkelräta axeln. |
| [get_CrossesAt](./get_crossesat/)() | Anger var på den vinkelräta axeln axeln korsar. |
| [get_DisplayUnit](./get_displayunit/)() | Anger skalningsvärdet för visningsenheterna för värdeaxeln. |
| [get_Document](./get_document/)() | Returnerar dokumentet som innehåller det överordnade diagrammet. |
| [get_Format](./get_format/)() | Tillhandahåller åtkomst till linjeformatering för axeln och fyllning av tick‑etiketterna. |
| [get_HasMajorGridlines](./get_hasmajorgridlines/)() | Hämtar eller anger en flagga som indikerar om axeln har huvudrutnät. |
| [get_HasMinorGridlines](./get_hasminorgridlines/)() | Hämtar eller anger en flagga som indikerar om axeln har sekundära rutnät. |
| [get_Hidden](./get_hidden/)() | Hämtar eller anger en flagga som indikerar om denna axel är dold eller inte. |
| [get_MajorTickMark](./get_majortickmark/)() | Returnerar eller anger huvud‑tick‑markeringarna. |
| [get_MajorUnit](./get_majorunit/)() | Returnerar eller anger avståndet mellan huvud‑tick‑markeringarna. |
| [get_MajorUnitIsAuto](./get_majorunitisauto/)() | Hämtar eller anger en flagga som indikerar om standardavståndet mellan huvud‑tick‑markeringar ska användas. |
| [get_MajorUnitScale](./get_majorunitscale/)() | Returnerar eller anger skalvärdet för huvud‑tick‑markeringar på tidskategori‑axeln. |
| [get_MinorTickMark](./get_minortickmark/)() | Returnerar eller anger sekundära tick‑markeringar för axeln. |
| [get_MinorUnit](./get_minorunit/)() | Returnerar eller anger avståndet mellan sekundära tick‑markeringar. |
| [get_MinorUnitIsAuto](./get_minorunitisauto/)() | Hämtar eller anger en flagga som indikerar om standardavståndet mellan sekundära tick‑markeringar ska användas. |
| [get_MinorUnitScale](./get_minorunitscale/)() | Returnerar eller anger skalvärdet för sekundära tick‑markeringar på tidskategori‑axeln. |
| [get_NumberFormat](./get_numberformat/)() | Returnerar ett [ChartNumberFormat](../chartnumberformat/)‑objekt som möjliggör att definiera talformat för axeln. |
| [get_ReverseOrder](./get_reverseorder/)() | Returnerar eller anger en flagga som indikerar om axelvärdena ska visas i omvänd ordning, d.v.s. från max till min. |
| [get_Scaling](./get_scaling/)() | Tillhandahåller åtkomst till skalningsalternativen för axeln. |
| [get_TickLabels](./get_ticklabels/)() | Tillhandahåller åtkomst till egenskaperna för axelns tick‑etikettmarkeringar. |
| [get_TickMarkSpacing](./get_tickmarkspacing/)() | Hämtar eller anger intervallet där tick‑markeringar ritas. |
| [get_Title](./get_title/)() | Tillhandahåller åtkomst till axelns titel‑egenskaper. |
| [get_Type](./get_type/)() const | Returnerar axelns typ. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_AxisBetweenCategories](./set_axisbetweencategories/)(bool) | Sättare för [Aspose::Words::Drawing::Charts::ChartAxis::get_AxisBetweenCategories](./get_axisbetweencategories/). |
| [set_BaseTimeUnit](./set_basetimeunit/)(Aspose::Words::Drawing::Charts::AxisTimeUnit) | Sättare för [Aspose::Words::Drawing::Charts::ChartAxis::get_BaseTimeUnit](./get_basetimeunit/). |
| [set_CategoryType](./set_categorytype/)(Aspose::Words::Drawing::Charts::AxisCategoryType) | Sättare för [Aspose::Words::Drawing::Charts::ChartAxis::get_CategoryType](./get_categorytype/). |
| [set_Crosses](./set_crosses/)(Aspose::Words::Drawing::Charts::AxisCrosses) | Sättare för [Aspose::Words::Drawing::Charts::ChartAxis::get_Crosses](./get_crosses/). |
| [set_CrossesAt](./set_crossesat/)(double) | Sättare för [Aspose::Words::Drawing::Charts::ChartAxis::get_CrossesAt](./get_crossesat/). |
| [set_HasMajorGridlines](./set_hasmajorgridlines/)(bool) | Sättare för [Aspose::Words::Drawing::Charts::ChartAxis::get_HasMajorGridlines](./get_hasmajorgridlines/). |
| [set_HasMinorGridlines](./set_hasminorgridlines/)(bool) | Sättare för [Aspose::Words::Drawing::Charts::ChartAxis::get_HasMinorGridlines](./get_hasminorgridlines/). |
| [set_Hidden](./set_hidden/)(bool) | Sättare för [Aspose::Words::Drawing::Charts::ChartAxis::get_Hidden](./get_hidden/). |
| [set_MajorTickMark](./set_majortickmark/)(Aspose::Words::Drawing::Charts::AxisTickMark) | Sättare för [Aspose::Words::Drawing::Charts::ChartAxis::get_MajorTickMark](./get_majortickmark/). |
| [set_MajorUnit](./set_majorunit/)(double) | Sättare för [Aspose::Words::Drawing::Charts::ChartAxis::get_MajorUnit](./get_majorunit/). |
| [set_MajorUnitIsAuto](./set_majorunitisauto/)(bool) | Sättare för [Aspose::Words::Drawing::Charts::ChartAxis::get_MajorUnitIsAuto](./get_majorunitisauto/). |
| [set_MajorUnitScale](./set_majorunitscale/)(Aspose::Words::Drawing::Charts::AxisTimeUnit) | Sättare för [Aspose::Words::Drawing::Charts::ChartAxis::get_MajorUnitScale](./get_majorunitscale/). |
| [set_MinorTickMark](./set_minortickmark/)(Aspose::Words::Drawing::Charts::AxisTickMark) | Sättare för [Aspose::Words::Drawing::Charts::ChartAxis::get_MinorTickMark](./get_minortickmark/). |
| [set_MinorUnit](./set_minorunit/)(double) | Sättare för [Aspose::Words::Drawing::Charts::ChartAxis::get_MinorUnit](./get_minorunit/). |
| [set_MinorUnitIsAuto](./set_minorunitisauto/)(bool) | Sättare för [Aspose::Words::Drawing::Charts::ChartAxis::get_MinorUnitIsAuto](./get_minorunitisauto/). |
| [set_MinorUnitScale](./set_minorunitscale/)(Aspose::Words::Drawing::Charts::AxisTimeUnit) | Sättare för [Aspose::Words::Drawing::Charts::ChartAxis::get_MinorUnitScale](./get_minorunitscale/). |
| [set_ReverseOrder](./set_reverseorder/)(bool) | Sättare för [Aspose::Words::Drawing::Charts::ChartAxis::get_ReverseOrder](./get_reverseorder/). |
| [set_TickMarkSpacing](./set_tickmarkspacing/)(int32_t) | Sättare för [Aspose::Words::Drawing::Charts::ChartAxis::get_TickMarkSpacing](./get_tickmarkspacing/). |
| static [Type](./type/)() |  |

## Exempel



Visar hur man infogar ett diagram och ändrar utseendet på dess axlar.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 500, 300);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();

// Rensa diagrammets demodata-serie för att börja med ett rent diagram.
chart->get_Series()->Clear();

// Infoga en diagramserie med kategorier för X‑axeln och respektive numeriska värden för Y‑axeln.
chart->get_Series()->Add(u"Aspose Test Series", System::MakeArray<System::String>({u"Word", u"PDF", u"Excel", u"GoogleDocs", u"Note"}), System::MakeArray<double>({640, 320, 280, 120, 150}));

// Diagramaxlar har olika alternativ som kan ändra deras utseende,
// såsom deras riktning, huvud-/delstegsenheter och tick‑markeringar.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartAxis> xAxis = chart->get_AxisX();
xAxis->set_CategoryType(Aspose::Words::Drawing::Charts::AxisCategoryType::Category);
xAxis->set_Crosses(Aspose::Words::Drawing::Charts::AxisCrosses::Minimum);
xAxis->set_ReverseOrder(false);
xAxis->set_MajorTickMark(Aspose::Words::Drawing::Charts::AxisTickMark::Inside);
xAxis->set_MinorTickMark(Aspose::Words::Drawing::Charts::AxisTickMark::Cross);
xAxis->set_MajorUnit(10.0);
xAxis->set_MinorUnit(15.0);
xAxis->get_TickLabels()->set_Offset(50);
xAxis->get_TickLabels()->set_Position(Aspose::Words::Drawing::Charts::AxisTickLabelPosition::Low);
xAxis->get_TickLabels()->set_IsAutoSpacing(false);
xAxis->set_TickMarkSpacing(1);

ASPOSE_ASSERT_EQ(doc, xAxis->get_Document());

System::SharedPtr<Aspose::Words::Drawing::Charts::ChartAxis> yAxis = chart->get_AxisY();
yAxis->set_CategoryType(Aspose::Words::Drawing::Charts::AxisCategoryType::Automatic);
yAxis->set_Crosses(Aspose::Words::Drawing::Charts::AxisCrosses::Maximum);
yAxis->set_ReverseOrder(true);
yAxis->set_MajorTickMark(Aspose::Words::Drawing::Charts::AxisTickMark::Inside);
yAxis->set_MinorTickMark(Aspose::Words::Drawing::Charts::AxisTickMark::Cross);
yAxis->set_MajorUnit(100.0);
yAxis->set_MinorUnit(20.0);
yAxis->get_TickLabels()->set_Position(Aspose::Words::Drawing::Charts::AxisTickLabelPosition::NextToAxis);
yAxis->get_TickLabels()->set_Alignment(Aspose::Words::ParagraphAlignment::Center);
yAxis->get_TickLabels()->get_Font()->set_Color(System::Drawing::Color::get_Red());
yAxis->get_TickLabels()->set_Spacing(1);

// Stapeldiagram har ingen Z‑axel.
ASSERT_TRUE(System::TestTools::IsNull(chart->get_AxisZ()));

doc->Save(get_ArtifactsDir() + u"Charts.AxisProperties.docx");
```

## Se även

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
