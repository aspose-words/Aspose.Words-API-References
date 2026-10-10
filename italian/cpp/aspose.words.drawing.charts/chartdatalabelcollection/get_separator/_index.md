---
title: "Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_Separator method"
linktitle: "Aspose::Words::Fields::FieldMergeBarcode::get_ScalingFactor metodo"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_Separator method. Ottiene o imposta il separatore di stringa utilizzato per le etichette dei dati dell'intera serie. Il valore predefinito è una virgola, eccetto per i grafici a torta che mostrano solo il nome della categoria e la percentuale, quando invece deve essere usata un'interruzione di riga in C++."
type: docs
weight: 6000
url: /it/cpp/aspose.words.drawing.charts/chartdatalabelcollection/get_separator/
---
## ChartDataLabelCollection::get_Separator method


Ottiene o imposta il separatore di stringa utilizzato per le etichette dati dell'intera serie. Il valore predefinito è una virgola, eccetto per i grafici a torta che mostrano solo il nome della categoria e la percentuale, dove viene usata una interruzione di riga.

```cpp
System::String Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_Separator()
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


Mostra come lavorare con le etichette dei dati di un grafico a torta.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Pie, 500, 300)->get_Chart();

// Cancella la serie di dati demo del grafico per iniziare con un grafico pulito.
chart->get_Series()->Clear();

// Inserisci una serie di grafico personalizzata con un nome di categoria per ciascuno dei settori e la loro tabella di frequenza.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series = chart->get_Series()->Add(u"Aspose Test Series", System::MakeArray<System::String>({u"Word", u"PDF", u"Excel"}), System::MakeArray<double>({2.7, 3.2, 0.8}));

// Abilita le etichette dei dati che visualizzeranno sia la percentuale sia la frequenza di ciascun settore e modifica il loro aspetto.
series->set_HasDataLabels(true);
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartDataLabelCollection> dataLabels = series->get_DataLabels();
dataLabels->set_ShowLeaderLines(true);
dataLabels->set_ShowLegendKey(true);
dataLabels->set_ShowPercentage(true);
dataLabels->set_ShowValue(true);
dataLabels->set_Separator(u"; ");

doc->Save(get_ArtifactsDir() + u"Charts.DataLabelsPieChart.docx");
```

## Vedi anche

* Class [ChartDataLabelCollection](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
