---
title: "Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_FirstSliceAngle Methode"
linktitle: "get_FirstSliceAngle"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_FirstSliceAngle Methode. Liest oder setzt den Winkel in Grad des ersten Abschnitts des übergeordneten Kreisdiagramms in C++."
type: docs
weight: 7000
url: /de/cpp/aspose.words.drawing.charts/chartseriesgroup/get_firstsliceangle/
---
## ChartSeriesGroup::get_FirstSliceAngle method


Liest oder legt den Winkel (in Grad) des ersten Stücks des übergeordneten Kreisdiagramms fest.

```cpp
int32_t Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_FirstSliceAngle()
```

## Hinweise


Gilt für Seriengruppen der Typen [Pie](../../chartseriestype/), [Pie3D](../../chartseriestype/) und [Doughnut](../../chartseriestype/).

Der zulässige Wertebereich liegt zwischen 0 und 360 inklusive. Der Standardwert ist 0.

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
