---
title: "Aspose::Words::Drawing::Charts::ChartDataLabel::get_Position-Methode"
linktitle: "get_Position"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::Charts::ChartDataLabel::get_Position-Methode. Ruft die Position der Datenbeschriftung ab oder legt sie fest in C++."
type: docs
weight: 7501
url: /de/cpp/aspose.words.drawing.charts/chartdatalabel/get_position/
---
## ChartDataLabel::get_Position method


Liest oder setzt die Position der Datenbeschriftung.

```cpp
Aspose::Words::Drawing::Charts::ChartDataLabelPosition Aspose::Words::Drawing::Charts::ChartDataLabel::get_Position()
```

## Hinweise


Die Position kann für Datenbeschriftungen der folgenden Diagrammserientypen festgelegt werden:

* [Bar](../../chartseriestype/), [Column](../../chartseriestype/), [Histogram](../../chartseriestype/), [Pareto](../../chartseriestype/), [Waterfall](../../chartseriestype/); allowed values: [Center](../../chartdatalabelposition/), [InsideBase](../../chartdatalabelposition/), [InsideEnd](../../chartdatalabelposition/) and [OutsideEnd](../../chartdatalabelposition/);
* [BarStacked](../../chartseriestype/), [BarPercentStacked](../../chartseriestype/), [ColumnStacked](../../chartseriestype/), [ColumnPercentStacked](../../chartseriestype/); allowed values: [Center](../../chartdatalabelposition/), [InsideBase](../../chartdatalabelposition/) and [InsideEnd](../../chartdatalabelposition/);
* [Bubble](../../chartseriestype/), [Bubble3D](../../chartseriestype/), [Line](../../chartseriestype/), [LineStacked](../../chartseriestype/), [LinePercentStacked](../../chartseriestype/), [Scatter](../../chartseriestype/), [Stock](../../chartseriestype/); allowed values: [Center](../../chartdatalabelposition/), [Left](../../chartdatalabelposition/), [Right](../../chartdatalabelposition/), [Above](../../chartdatalabelposition/) and [Below](../../chartdatalabelposition/);
* [Pie](../../chartseriestype/), [Pie3D](../../chartseriestype/), [PieOfBar](../../chartseriestype/), [PieOfPie](../../chartseriestype/); allowed values: [Center](../../chartdatalabelposition/), [InsideEnd](../../chartdatalabelposition/), [OutsideEnd](../../chartdatalabelposition/) and [BestFit](../../chartdatalabelposition/);
* [BoxAndWhisker](../../chartseriestype/); allowed values: [Left](../../chartdatalabelposition/), [Right](../../chartdatalabelposition/), [Above](../../chartdatalabelposition/) and [Below](../../chartdatalabelposition/).



## Beispiele



Zeigt, wie die Position der Datenbeschriftung festgelegt wird.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// SpaltenDiagramm einfügen.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 432, 252);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeriesCollection> seriesColl = chart->get_Series();

// Lösche standardmäßig generierte Serie.
seriesColl->Clear();

// Serie hinzufügen.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series = seriesColl->Add(u"Series 1", System::MakeArray<System::String>({u"Category 1", u"Category 2", u"Category 3"}), System::MakeArray<double>({4, 5, 6}));

// Datenbeschriftungen anzeigen und Schriftfarbe festlegen.
series->set_HasDataLabels(true);
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartDataLabelCollection> dataLabels = series->get_DataLabels();
dataLabels->set_ShowValue(true);
dataLabels->get_Font()->set_Color(System::Drawing::Color::get_White());

// Position der Datenbeschriftung festlegen.
dataLabels->set_Position(Aspose::Words::Drawing::Charts::ChartDataLabelPosition::InsideBase);
dataLabels->idx_get(0)->set_Position(Aspose::Words::Drawing::Charts::ChartDataLabelPosition::OutsideEnd);
dataLabels->idx_get(0)->get_Font()->set_Color(System::Drawing::Color::get_DarkRed());

doc->Save(get_ArtifactsDir() + u"Charts.LabelPosition.docx");
```

## Siehe auch

* Enum [ChartDataLabelPosition](../../chartdatalabelposition/)
* Class [ChartDataLabel](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
