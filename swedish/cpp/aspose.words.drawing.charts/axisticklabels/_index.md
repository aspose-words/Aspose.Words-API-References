---
title: "Aspose::Words::Drawing::Charts::AxisTickLabels-klass"
linktitle: "AxisTickLabels"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Drawing::Charts::AxisTickLabels-klass. Representerar egenskaper för axelns tick-märkesetiketter i C++."
type: docs
weight: 3250
url: /sv/cpp/aspose.words.drawing.charts/axisticklabels/
---
## AxisTickLabels class


Representerar egenskaper för axelns tick-markeringsetiketter.

```cpp
class AxisTickLabels : public Aspose::Words::Drawing::Charts::Core::IChartItemTextProperties
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [get_Alignment](./get_alignment/)() | Hämtar eller anger textjustering för axelns tick-etiketter. |
| [get_Font](./get_font/)() | Tillhandahåller åtkomst till teckensnittsformatering för tick-etiketterna. |
| [get_IsAutoSpacing](./get_isautospacing/)() | Hämtar eller anger en flagga som indikerar om ett automatiskt intervall ska användas för att rita tick-etiketterna. |
| [get_Offset](./get_offset/)() | Hämtar eller anger avståndet för tick-etiketterna från axeln. |
| [get_Orientation](./get_orientation/)() | Hämtar eller anger orienteringen för tick-etiketttexten. |
| [get_Position](./get_position/)() | Hämtar eller anger positionen för tick-etiketterna på axeln. |
| [get_Rotation](./get_rotation/)() | Hämtar eller anger rotationen för tick-etiketterna i grader. |
| [get_Spacing](./get_spacing/)() | Hämtar eller anger intervallet då tick-etiketterna ritas. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Alignment](./set_alignment/)(Aspose::Words::ParagraphAlignment) | Sättare för [Aspose::Words::Drawing::Charts::AxisTickLabels::get_Alignment](./get_alignment/). |
| [set_IsAutoSpacing](./set_isautospacing/)(bool) | Sättare för [Aspose::Words::Drawing::Charts::AxisTickLabels::get_IsAutoSpacing](./get_isautospacing/). |
| [set_Offset](./set_offset/)(int32_t) | Inställningsmetod för [Aspose::Words::Drawing::Charts::AxisTickLabels::get_Offset](./get_offset/). |
| [set_Orientation](./set_orientation/)(Aspose::Words::Drawing::ShapeTextOrientation) | Inställningsmetod för [Aspose::Words::Drawing::Charts::AxisTickLabels::get_Orientation](./get_orientation/). |
| [set_Position](./set_position/)(Aspose::Words::Drawing::Charts::AxisTickLabelPosition) | Inställningsmetod för [Aspose::Words::Drawing::Charts::AxisTickLabels::get_Position](./get_position/). |
| [set_Rotation](./set_rotation/)(int32_t) | Inställningsmetod för [Aspose::Words::Drawing::Charts::AxisTickLabels::get_Rotation](./get_rotation/). |
| [set_Spacing](./set_spacing/)(int32_t) | Inställningsmetod för [Aspose::Words::Drawing::Charts::AxisTickLabels::get_Spacing](./get_spacing/). |
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
