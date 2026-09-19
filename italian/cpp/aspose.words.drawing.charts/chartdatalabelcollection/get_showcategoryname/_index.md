---
title: "Metodo Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_ShowCategoryName"
linktitle: "get_ShowCategoryName"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_ShowCategoryName. Consente di specificare se il nome della categoria deve essere visualizzato per le etichette dei dati dell'intera serie. Il valore predefinito è false in C++."
type: docs
weight: 8000
url: /it/cpp/aspose.words.drawing.charts/chartdatalabelcollection/get_showcategoryname/
---
## ChartDataLabelCollection::get_ShowCategoryName method


Consente di specificare se visualizzare il nome della categoria per le etichette dati dell'intera serie. Il valore predefinito è **false**.

```cpp
bool Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_ShowCategoryName()
```


## Esempi



Mostra come lavorare con le etichette dei dati di un grafico a bolle.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Bubble, 500, 300)->get_Chart();

// Cancella la serie di dati demo del grafico per iniziare con un grafico pulito.
chart->get_Series()->Clear();

// Aggiungi una serie personalizzata con coordinate X/Y e diametro di ciascuna bolla.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series = chart->get_Series()->Add(u"Aspose Test Series", System::MakeArray<double>({2.9, 3.5, 1.1, 4.0, 4.0}), System::MakeArray<double>({1.9, 8.5, 2.1, 6.0, 1.5}), System::MakeArray<double>({9.0, 4.5, 2.5, 8.0, 5.0}));

// Abilita le etichette dei dati, quindi modifica il loro aspetto.
series->set_HasDataLabels(true);
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartDataLabelCollection> dataLabels = series->get_DataLabels();
dataLabels->set_ShowBubbleSize(true);
dataLabels->set_ShowCategoryName(true);
dataLabels->set_ShowSeriesName(true);
dataLabels->set_Separator(u" & ");

doc->Save(get_ArtifactsDir() + u"Charts.DataLabelsBubbleChart.docx");
```

## Vedi anche

* Class [ChartDataLabelCollection](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
