---
title: "Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_SecondSectionSize metodo"
linktitle: "get_SecondSectionSize"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_SecondSectionSize method. Ottiene o imposta la dimensione della sezione secondaria del grafico a torta come percentuale in C++."
type: docs
weight: 10000
url: /it/cpp/aspose.words.drawing.charts/chartseriesgroup/get_secondsectionsize/
---
## ChartSeriesGroup::get_SecondSectionSize method


Ottiene o imposta la dimensione della sezione secondaria del grafico a torta come percentuale.

```cpp
int32_t Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_SecondSectionSize()
```

## Note


Si applica ai gruppi di serie dei tipi [PieOfPie](../../chartseriestype/) e [PieOfBar](../../chartseriestype/).

L'intervallo di valori accettabili è da 5 a 200 inclusi. Il valore predefinito è 75.

## Esempi



Mostra come creare e formattare il grafico Pie of Pie.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::PieOfPie, 440, 300);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();
// Elimina la serie generata per impostazione predefinita.
chart->get_Series()->Clear();

auto categories = System::MakeArray<System::String>({u"Category 1", u"Category 2", u"Category 3", u"Category 4"});
chart->get_Series()->Add(u"Series 1", categories, System::MakeArray<double>({11, 8, 4, 3}));

// Formatta il grafico Pie of Pie.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeriesGroup> seriesGroup = chart->get_SeriesGroups()->idx_get(0);
seriesGroup->set_GapWidth(10);
seriesGroup->set_SecondSectionSize(77);

doc->Save(get_ArtifactsDir() + u"Charts.PieOfPieChart.docx");
```

## Vedi anche

* Class [ChartSeriesGroup](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
