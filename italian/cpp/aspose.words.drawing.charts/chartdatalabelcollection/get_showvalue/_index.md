---
title: "Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_ShowValue metodo"
linktitle: "get_ShowValue"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_ShowValue metodo. Consente di specificare se i valori devono essere visualizzati nelle etichette dei dati dell'intera serie. Il valore predefinito è false in C++."
type: docs
weight: 14000
url: /it/cpp/aspose.words.drawing.charts/chartdatalabelcollection/get_showvalue/
---
## ChartDataLabelCollection::get_ShowValue method


Consente di specificare se visualizzare i valori nelle etichette dati dell'intera serie. Il valore predefinito è **false**.

```cpp
bool Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_ShowValue()
```


## Esempi



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
