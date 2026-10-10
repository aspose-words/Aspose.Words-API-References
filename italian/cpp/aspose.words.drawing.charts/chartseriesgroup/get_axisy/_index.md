---
title: "Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_AxisY metodo"
linktitle: "get_AxisY"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_AxisY metodo. Fornisce l'accesso alle proprietà dell'asse Y di questo gruppo di serie in C++."
type: docs
weight: 4000
url: /it/cpp/aspose.words.drawing.charts/chartseriesgroup/get_axisy/
---
## ChartSeriesGroup::get_AxisY method


Fornisce l'accesso alle proprietà dell'asse Y di questo gruppo di serie.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartAxis> Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_AxisY()
```


## Esempi



Mostra come lavorare con l'asse secondario del grafico.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Line, 450, 250);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeriesCollection> series = chart->get_Series();

// Elimina la serie generata di default.
series->Clear();

auto categories = System::MakeArray<System::String>({u"Category 1", u"Category 2", u"Category 3"});
series->Add(u"Series 1 of primary series group", categories, System::MakeArray<double>({2, 3, 4}));
series->Add(u"Series 2 of primary series group", categories, System::MakeArray<double>({5, 2, 3}));

// Crea un gruppo di serie aggiuntivo, anch'esso di tipo linea.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeriesGroup> newSeriesGroup = chart->get_SeriesGroups()->Add(Aspose::Words::Drawing::Charts::ChartSeriesType::Line);
// Specifica l'uso degli assi secondari per il nuovo gruppo di serie.
newSeriesGroup->set_AxisGroup(Aspose::Words::Drawing::Charts::AxisGroup::Secondary);
// Nascondi l'asse X secondario.
newSeriesGroup->get_AxisX()->set_Hidden(true);
// Definisci il titolo dell'asse Y secondario.
newSeriesGroup->get_AxisY()->get_Title()->set_Show(true);
newSeriesGroup->get_AxisY()->get_Title()->set_Text(u"Secondary Y axis");

ASSERT_EQ(Aspose::Words::Drawing::Charts::ChartSeriesType::Line, newSeriesGroup->get_SeriesType());

// Aggiungi una serie al nuovo gruppo di serie.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series3 = newSeriesGroup->get_Series()->Add(u"Series of secondary series group", categories, System::MakeArray<double>({13, 11, 16}));
series3->get_Format()->get_Stroke()->set_Weight(3.5);

doc->Save(get_ArtifactsDir() + u"Charts.SecondaryAxis.docx");
```

## Vedi anche

* Class [ChartAxis](../../chartaxis/)
* Class [ChartSeriesGroup](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
