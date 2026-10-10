---
title: "Aspose::Words::Drawing::Charts::ChartDataLabelPosition enum"
linktitle: "ChartDataLabelPosition"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::Charts::ChartDataLabelPosition enum. Gibt die Position für eine Diagrammdatenbeschriftung in C++ an."
type: docs
weight: 27334
url: /de/cpp/aspose.words.drawing.charts/chartdatalabelposition/
---
## ChartDataLabelPosition enum


Gibt die Position einer Diagrammdatenbeschriftung an.

```cpp
enum class ChartDataLabelPosition
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Mitte | 0 | Gibt an, dass eine Datenbeschriftung zentriert auf einem Datenmarker angezeigt werden soll. |
| Links | 1 | Gibt an, dass eine Datenbeschriftung links von einem Datenmarker angezeigt werden soll. |
| Rechts | 2 | Gibt an, dass eine Datenbeschriftung rechts von einem Datenmarker angezeigt werden soll. |
| Oben | 3 | Gibt an, dass eine Datenbeschriftung über einem Datenmarker angezeigt werden soll. |
| Unten | 4 | Gibt an, dass eine Datenbeschriftung unter einem Datenmarker angezeigt werden soll. |
| InsideBase | 5 | Gibt an, dass eine Datenbeschriftung innerhalb der Basis eines Datenmarkers angezeigt werden soll. |
| InsideEnd | 6 | Gibt an, dass eine Datenbeschriftung innerhalb des Endes eines Datenmarkers angezeigt werden soll. |
| OutsideEnd | 7 | Gibt an, dass eine Datenbeschriftung außerhalb des Endes eines Datenmarkers angezeigt werden soll. |
| BestFit | 8 | Gibt an, dass eine Datenbeschriftung in der am besten geeigneten Position angezeigt werden soll. |


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

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
