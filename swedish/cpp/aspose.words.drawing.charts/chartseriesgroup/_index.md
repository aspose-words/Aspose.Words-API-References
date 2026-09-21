---
title: "Aspose::Words::Drawing::Charts::ChartSeriesGroup klass"
linktitle: "ChartSeriesGroup"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Drawing::Charts::ChartSeriesGroup klass. Representerar egenskaper för en diagramseriegrupp, det vill säga egenskaperna för diagramserier av samma typ som är associerade med samma axlar i C++."
type: docs
weight: 17334
url: /sv/cpp/aspose.words.drawing.charts/chartseriesgroup/
---
## ChartSeriesGroup class


Representerar egenskaper för en diagramseriegrupp, det vill säga egenskaperna för diagramserier av samma typ som är kopplade till samma axlar.

```cpp
class ChartSeriesGroup : public System::Object
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [get_AxisGroup](./get_axisgroup/)() | Hämtar eller anger axelgruppen som denna seriegrupp tillhör. |
| [get_AxisX](./get_axisx/)() | Tillhandahåller åtkomst till egenskaper för X-axeln i denna seriegrupp. |
| [get_AxisY](./get_axisy/)() | Tillhandahåller åtkomst till egenskaper för Y-axeln i denna seriegrupp. |
| [get_BubbleScale](./get_bubblescale/)() | Hämtar eller anger storleken på bubblorna som en procentandel av deras standardstorlek. |
| [get_DoughnutHoleSize](./get_doughnutholesize/)() | Hämtar eller anger hålstorleken för det överordnade ringdiagrammet som en procentandel. |
| [get_FirstSliceAngle](./get_firstsliceangle/)() | Hämtar eller anger vinkeln, i grader, för den första skivan i det överordnade cirkeldiagrammet. |
| [get_GapWidth](./get_gapwidth/)() | Hämtar eller anger procentandelen av mellanrumets bredd mellan diagramelement. |
| [get_Overlap](./get_overlap/)() | Hämtar eller anger procentandelen av hur mycket seriernas staplar eller kolumner överlappar. |
| [get_SecondSectionSize](./get_secondsectionsize/)() | Hämtar eller anger storleken på cirkeldiagrammets sekundära sektion som en procentandel. |
| [get_Series](./get_series/)() | Hämtar en samling av serier som tillhör denna seriegrupp. |
| [get_SeriesType](./get_seriestype/)() | Hämtar typen av diagramserie som ingår i denna grupp. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_AxisGroup](./set_axisgroup/)(Aspose::Words::Drawing::Charts::AxisGroup) | Sättare för [Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_AxisGroup](./get_axisgroup/). |
| [set_BubbleScale](./set_bubblescale/)(int32_t) | Sättare för [Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_BubbleScale](./get_bubblescale/). |
| [set_DoughnutHoleSize](./set_doughnutholesize/)(int32_t) | Sättare för [Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_DoughnutHoleSize](./get_doughnutholesize/). |
| [set_FirstSliceAngle](./set_firstsliceangle/)(int32_t) | Sättare för [Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_FirstSliceAngle](./get_firstsliceangle/). |
| [set_GapWidth](./set_gapwidth/)(int32_t) | Sättare för [Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_GapWidth](./get_gapwidth/). |
| [set_Overlap](./set_overlap/)(int32_t) | Sättare för [Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_Overlap](./get_overlap/). |
| [set_SecondSectionSize](./set_secondsectionsize/)(int32_t) | Sättare för [Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_SecondSectionSize](./get_secondsectionsize/). |
| static [Type](./type/)() |  |
## Anmärkningar


Kombinationsdiagram innehåller flera diagramseriegrupper, med en separat grupp för varje serietyp.

Du kan också skapa en diagramseriegrupp för att tilldela sekundära axlar till en eller flera diagramserier.

För att lära dig mer, besök dokumentationsartikeln [Working with Charts](https://docs.aspose.com/words/cpp/working-with-charts/).

## Exempel



Visar hur man arbetar med diagrammets sekundära axel.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Line, 450, 250);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeriesCollection> series = chart->get_Series();

// Ta bort standardgenererad serie.
series->Clear();

auto categories = System::MakeArray<System::String>({u"Category 1", u"Category 2", u"Category 3"});
series->Add(u"Series 1 of primary series group", categories, System::MakeArray<double>({2, 3, 4}));
series->Add(u"Series 2 of primary series group", categories, System::MakeArray<double>({5, 2, 3}));

// Skapa en ytterligare seriegrupp, också av linjetyp.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeriesGroup> newSeriesGroup = chart->get_SeriesGroups()->Add(Aspose::Words::Drawing::Charts::ChartSeriesType::Line);
// Specificera användningen av sekundära axlar för den nya seriegruppen.
newSeriesGroup->set_AxisGroup(Aspose::Words::Drawing::Charts::AxisGroup::Secondary);
// Dölj den sekundära X-axeln.
newSeriesGroup->get_AxisX()->set_Hidden(true);
// Definiera titel för den sekundära Y-axeln.
newSeriesGroup->get_AxisY()->get_Title()->set_Show(true);
newSeriesGroup->get_AxisY()->get_Title()->set_Text(u"Secondary Y axis");

ASSERT_EQ(Aspose::Words::Drawing::Charts::ChartSeriesType::Line, newSeriesGroup->get_SeriesType());

// Lägg till en serie i den nya seriegruppen.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series3 = newSeriesGroup->get_Series()->Add(u"Series of secondary series group", categories, System::MakeArray<double>({13, 11, 16}));
series3->get_Format()->get_Stroke()->set_Weight(3.5);

doc->Save(get_ArtifactsDir() + u"Charts.SecondaryAxis.docx");
```

## Se även

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
