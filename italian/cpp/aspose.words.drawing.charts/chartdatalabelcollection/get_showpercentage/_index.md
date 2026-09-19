---
title: "Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_ShowPercentage metodo"
linktitle: "get_ShowPercentage"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_ShowPercentage metodo. Consente di specificare se visualizzare il valore percentuale per le etichette dei dati dell'intera serie. Il valore predefinito è false. Si applica solo ai grafici a torta in C++."
type: docs
weight: 12000
url: /it/cpp/aspose.words.drawing.charts/chartdatalabelcollection/get_showpercentage/
---
## ChartDataLabelCollection::get_ShowPercentage method


Consente di specificare se visualizzare il valore percentuale per le etichette dati dell'intera serie. Il valore predefinito è **false**. Si applica solo ai grafici a torta.

```cpp
bool Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_ShowPercentage()
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
