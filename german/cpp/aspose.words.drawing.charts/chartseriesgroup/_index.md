---
title: "Aspose::Words::Drawing::Charts::ChartSeriesGroup Klasse"
linktitle: "ChartSeriesGroup"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::Charts::ChartSeriesGroup Klasse. Stellt Eigenschaften einer Diagramm‑Seriengruppe dar, d. h. die Eigenschaften von Diagrammserien desselben Typs, die denselben Achsen in C++ zugeordnet sind."
type: docs
weight: 17334
url: /de/cpp/aspose.words.drawing.charts/chartseriesgroup/
---
## ChartSeriesGroup class


Stellt Eigenschaften einer Diagrammreihen‑Gruppe dar, d. h. die Eigenschaften von Diagrammreihen desselben Typs, die denselben Achsen zugeordnet sind.

```cpp
class ChartSeriesGroup : public System::Object
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [get_AxisGroup](./get_axisgroup/)() | Liest oder legt die Achsengruppe fest, zu der diese Seriengruppe gehört. |
| [get_AxisX](./get_axisx/)() | Stellt Zugriff auf die Eigenschaften der X‑Achse dieser Seriengruppe bereit. |
| [get_AxisY](./get_axisy/)() | Stellt Zugriff auf die Eigenschaften der Y‑Achse dieser Seriengruppe bereit. |
| [get_BubbleScale](./get_bubblescale/)() | Liest oder legt die Größe der Blasen als Prozentsatz ihrer Standardgröße fest. |
| [get_DoughnutHoleSize](./get_doughnutholesize/)() | Liest oder legt die Lochgröße des übergeordneten Donut‑Diagramms als Prozentsatz fest. |
| [get_FirstSliceAngle](./get_firstsliceangle/)() | Liest oder legt den Winkel (in Grad) des ersten Stücks des übergeordneten Kreisdiagramms fest. |
| [get_GapWidth](./get_gapwidth/)() | Liest oder legt den Prozentsatz der Lückenbreite zwischen Diagrammelementen fest. |
| [get_Overlap](./get_overlap/)() | Liest oder legt den Prozentsatz fest, wie stark die Serienbalken oder -spalten überlappen. |
| [get_SecondSectionSize](./get_secondsectionsize/)() | Liest oder legt die Größe des sekundären Abschnitts des Kreisdiagramms als Prozentsatz fest. |
| [get_Series](./get_series/)() | Ruft eine Sammlung von Serien ab, die zu dieser Seriengruppe gehören. |
| [get_SeriesType](./get_seriestype/)() | Ruft den Typ der in dieser Gruppe enthaltenen Diagrammserien ab. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_AxisGroup](./set_axisgroup/)(Aspose::Words::Drawing::Charts::AxisGroup) | Setter für [Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_AxisGroup](./get_axisgroup/). |
| [set_BubbleScale](./set_bubblescale/)(int32_t) | Setter für [Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_BubbleScale](./get_bubblescale/). |
| [set_DoughnutHoleSize](./set_doughnutholesize/)(int32_t) | Setter für [Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_DoughnutHoleSize](./get_doughnutholesize/). |
| [set_FirstSliceAngle](./set_firstsliceangle/)(int32_t) | Setter für [Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_FirstSliceAngle](./get_firstsliceangle/). |
| [set_GapWidth](./set_gapwidth/)(int32_t) | Setter für [Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_GapWidth](./get_gapwidth/). |
| [set_Overlap](./set_overlap/)(int32_t) | Setter für [Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_Overlap](./get_overlap/). |
| [set_SecondSectionSize](./set_secondsectionsize/)(int32_t) | Setter für [Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_SecondSectionSize](./get_secondsectionsize/). |
| static [Type](./type/)() |  |
## Hinweise


Kombinationsdiagramme enthalten mehrere Diagrammseriengruppen, wobei für jeden Serientyp eine separate Gruppe besteht.

Außerdem können Sie eine Diagrammseriengruppe erstellen, um sekundäre Achsen einem oder mehreren Diagrammserien zuzuweisen.

Weitere Informationen finden Sie im Dokumentationsartikel [Working with Charts](https://docs.aspose.com/words/cpp/working-with-charts/).

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

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
