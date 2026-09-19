---
title: "Metodo Aspose::Words::Drawing::Charts::ChartLegendEntry::get_IsHidden"
linktitle: "get_IsHidden"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Drawing::Charts::ChartLegendEntry::get_IsHidden. Ottiene o imposta un valore che indica se questa voce è nascosta nella legenda del grafico. Il valore predefinito è false in C++."
type: docs
weight: 3000
url: /it/cpp/aspose.words.drawing.charts/chartlegendentry/get_ishidden/
---
## ChartLegendEntry::get_IsHidden method


Ottiene o imposta un valore che indica se questa voce è nascosta nella legenda del grafico. Il valore predefinito è **false**.

```cpp
bool Aspose::Words::Drawing::Charts::ChartLegendEntry::get_IsHidden() const
```


## Esempi



Mostra come lavorare con una voce della legenda per le serie del grafico.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 432, 252);

System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeriesCollection> series = chart->get_Series();
series->Clear();

auto categories = System::MakeArray<System::String>({u"AW Category 1", u"AW Category 2"});

System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series1 = series->Add(u"Series 1", categories, System::MakeArray<double>({1, 2}));
series->Add(u"Series 2", categories, System::MakeArray<double>({3, 4}));
series->Add(u"Series 3", categories, System::MakeArray<double>({5, 6}));
series->Add(u"Series 4", categories, System::MakeArray<double>({0, 0}));

System::SharedPtr<Aspose::Words::Drawing::Charts::ChartLegendEntryCollection> legendEntries = chart->get_Legend()->get_LegendEntries();
legendEntries->idx_get(3)->set_IsHidden(true);

doc->Save(get_ArtifactsDir() + u"Charts.LegendEntries.docx");
```

## Vedi anche

* Class [ChartLegendEntry](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
