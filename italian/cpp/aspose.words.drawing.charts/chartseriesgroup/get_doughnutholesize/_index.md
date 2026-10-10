---
title: "Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_DoughnutHoleSize method"
linktitle: "get_DoughnutHoleSize"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_DoughnutHoleSize method. Ottiene o imposta la dimensione del foro del grafico a ciambella principale come percentuale in C++."
type: docs
weight: 6000
url: /it/cpp/aspose.words.drawing.charts/chartseriesgroup/get_doughnutholesize/
---
## ChartSeriesGroup::get_DoughnutHoleSize method


Ottiene o imposta la dimensione del foro del grafico a ciambella principale come percentuale.

```cpp
int32_t Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_DoughnutHoleSize()
```

## Note


Si applica solo ai gruppi di serie del tipo [Doughnut](../../chartseriestype/).

L'intervallo di valori accettabili è da 0 a 90 inclusi. Il valore predefinito è 75.

## Esempi



Mostra come creare e formattare il grafico Doughnut.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Doughnut, 400, 400);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();
// Elimina la serie generata per impostazione predefinita.
chart->get_Series()->Clear();

auto categories = System::MakeArray<System::String>({u"Category 1", u"Category 2", u"Category 3"});
chart->get_Series()->Add(u"Series 1", categories, System::MakeArray<double>({4, 2, 5}));

// Formatta il grafico Doughnut.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeriesGroup> seriesGroup = chart->get_SeriesGroups()->idx_get(0);
seriesGroup->set_DoughnutHoleSize(10);
seriesGroup->set_FirstSliceAngle(270);

doc->Save(get_ArtifactsDir() + u"Charts.DoughnutChart.docx");
```

## Vedi anche

* Class [ChartSeriesGroup](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
