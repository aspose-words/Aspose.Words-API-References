---
title: "Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_SecondSectionSize Methode"
linktitle: "get_SecondSectionSize"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_SecondSectionSize Methode. Gibt die Größe des sekundären Abschnitts des Kreisdiagramms als Prozentsatz zurück oder legt sie fest in C++."
type: docs
weight: 10000
url: /de/cpp/aspose.words.drawing.charts/chartseriesgroup/get_secondsectionsize/
---
## ChartSeriesGroup::get_SecondSectionSize method


Liest oder legt die Größe des sekundären Abschnitts des Kreisdiagramms als Prozentsatz fest.

```cpp
int32_t Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_SecondSectionSize()
```

## Hinweise


Gilt für Seriengruppen der Typen [PieOfPie](../../chartseriestype/) und [PieOfBar](../../chartseriestype/).

Der zulässige Wertebereich liegt zwischen 5 und 200 inklusive. Der Standardwert ist 75.

## Beispiele



Zeigt, wie man ein Pie-of-Pie-Diagramm erstellt und formatiert.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::PieOfPie, 440, 300);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();
// Löschen Sie die standardmäßig erzeugte Serie.
chart->get_Series()->Clear();

auto categories = System::MakeArray<System::String>({u"Category 1", u"Category 2", u"Category 3", u"Category 4"});
chart->get_Series()->Add(u"Series 1", categories, System::MakeArray<double>({11, 8, 4, 3}));

// Formatieren Sie das Pie-of-Pie-Diagramm.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeriesGroup> seriesGroup = chart->get_SeriesGroups()->idx_get(0);
seriesGroup->set_GapWidth(10);
seriesGroup->set_SecondSectionSize(77);

doc->Save(get_ArtifactsDir() + u"Charts.PieOfPieChart.docx");
```

## Siehe auch

* Class [ChartSeriesGroup](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
