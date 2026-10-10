---
title: "Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_DoughnutHoleSize Methode"
linktitle: "get_DoughnutHoleSize"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_DoughnutHoleSize Methode. Gibt die Lochgröße des übergeordneten Doughnut-Diagramms als Prozentsatz zurück oder legt sie fest in C++."
type: docs
weight: 6000
url: /de/cpp/aspose.words.drawing.charts/chartseriesgroup/get_doughnutholesize/
---
## ChartSeriesGroup::get_DoughnutHoleSize method


Liest oder legt die Lochgröße des übergeordneten Donut‑Diagramms als Prozentsatz fest.

```cpp
int32_t Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_DoughnutHoleSize()
```

## Hinweise


Gilt nur für Seriengruppen des Typs [Doughnut](../../chartseriestype/).

Der zulässige Wertebereich liegt zwischen 0 und 90 einschließlich. Der Standardwert ist 75.

## Beispiele



Zeigt, wie man ein Doughnut-Diagramm erstellt und formatiert.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Doughnut, 400, 400);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();
// Löschen Sie die standardmäßig erzeugte Serie.
chart->get_Series()->Clear();

auto categories = System::MakeArray<System::String>({u"Category 1", u"Category 2", u"Category 3"});
chart->get_Series()->Add(u"Series 1", categories, System::MakeArray<double>({4, 2, 5}));

// Formatieren Sie das Doughnut-Diagramm.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeriesGroup> seriesGroup = chart->get_SeriesGroups()->idx_get(0);
seriesGroup->set_DoughnutHoleSize(10);
seriesGroup->set_FirstSliceAngle(270);

doc->Save(get_ArtifactsDir() + u"Charts.DoughnutChart.docx");
```

## Siehe auch

* Class [ChartSeriesGroup](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
