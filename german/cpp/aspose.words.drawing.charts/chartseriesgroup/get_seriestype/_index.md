---
title: "Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_SeriesType Methode"
linktitle: "get_SeriesType"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_SeriesType Methode. Gibt den Typ der Diagrammserien zurück, die in dieser Gruppe enthalten sind, in C++."
type: docs
weight: 12000
url: /de/cpp/aspose.words.drawing.charts/chartseriesgroup/get_seriestype/
---
## ChartSeriesGroup::get_SeriesType method


Ruft den Typ der in dieser Gruppe enthaltenen Diagrammserien ab.

```cpp
Aspose::Words::Drawing::Charts::ChartSeriesType Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_SeriesType()
```


## Beispiele



Zeigt, wie man mit der sekundären Achse eines Diagramms arbeitet.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Line, 450, 250);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeriesCollection> series = chart->get_Series();

// Lösche standardmäßig generierte Serie.
series->Clear();

auto categories = System::MakeArray<System::String>({u"Category 1", u"Category 2", u"Category 3"});
series->Add(u"Series 1 of primary series group", categories, System::MakeArray<double>({2, 3, 4}));
series->Add(u"Series 2 of primary series group", categories, System::MakeArray<double>({5, 2, 3}));

// Erstellen Sie eine zusätzliche Seriengruppe, ebenfalls vom Typ Linie.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeriesGroup> newSeriesGroup = chart->get_SeriesGroups()->Add(Aspose::Words::Drawing::Charts::ChartSeriesType::Line);
// Geben Sie die Verwendung sekundärer Achsen für die neue Seriengruppe an.
newSeriesGroup->set_AxisGroup(Aspose::Words::Drawing::Charts::AxisGroup::Secondary);
// Blenden Sie die sekundäre X‑Achse aus.
newSeriesGroup->get_AxisX()->set_Hidden(true);
// Definieren Sie den Titel der sekundären Y‑Achse.
newSeriesGroup->get_AxisY()->get_Title()->set_Show(true);
newSeriesGroup->get_AxisY()->get_Title()->set_Text(u"Secondary Y axis");

ASSERT_EQ(Aspose::Words::Drawing::Charts::ChartSeriesType::Line, newSeriesGroup->get_SeriesType());

// Fügen Sie der neuen Seriengruppe eine Serie hinzu.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series3 = newSeriesGroup->get_Series()->Add(u"Series of secondary series group", categories, System::MakeArray<double>({13, 11, 16}));
series3->get_Format()->get_Stroke()->set_Weight(3.5);

doc->Save(get_ArtifactsDir() + u"Charts.SecondaryAxis.docx");
```

## Siehe auch

* Enum [ChartSeriesType](../../chartseriestype/)
* Class [ChartSeriesGroup](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
