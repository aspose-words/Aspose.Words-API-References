---
title: "Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_SecondSectionSize metod"
linktitle: "get_SecondSectionSize"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_SecondSectionSize metod. Hämtar eller anger storleken på pajdiagrammets sekundära sektion som en procentandel i C++."
type: docs
weight: 10000
url: /sv/cpp/aspose.words.drawing.charts/chartseriesgroup/get_secondsectionsize/
---
## ChartSeriesGroup::get_SecondSectionSize method


Hämtar eller anger storleken på cirkeldiagrammets sekundära sektion som en procentandel.

```cpp
int32_t Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_SecondSectionSize()
```

## Anmärkningar


Gäller för serieggrupper av typerna [PieOfPie](../../chartseriestype/) och [PieOfBar](../../chartseriestype/).

Det tillåtna värdeintervallet är från 5 till 200 inklusive. Standardvärdet är 75.

## Exempel



Visar hur man skapar och formaterar pie of Pie-diagram.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::PieOfPie, 440, 300);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();
// Ta bort den standardgenererade serien.
chart->get_Series()->Clear();

auto categories = System::MakeArray<System::String>({u"Category 1", u"Category 2", u"Category 3", u"Category 4"});
chart->get_Series()->Add(u"Series 1", categories, System::MakeArray<double>({11, 8, 4, 3}));

// Formatera Pie of Pie-diagrammet.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeriesGroup> seriesGroup = chart->get_SeriesGroups()->idx_get(0);
seriesGroup->set_GapWidth(10);
seriesGroup->set_SecondSectionSize(77);

doc->Save(get_ArtifactsDir() + u"Charts.PieOfPieChart.docx");
```

## Se även

* Class [ChartSeriesGroup](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
