---
title: "Aspose::Words::Drawing::Charts::ChartSeries::get_HasDataLabels metodo"
linktitle: "get_HasDataLabels"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Drawing::Charts::ChartSeries::get_HasDataLabels. Ottiene o imposta un flag che indica se le etichette dei dati sono visualizzate per la serie in C++."
type: docs
weight: 7000
url: /it/cpp/aspose.words.drawing.charts/chartseries/get_hasdatalabels/
---
## ChartSeries::get_HasDataLabels method


Ottiene o imposta un flag che indica se le etichette dei dati sono visualizzate per la serie.

```cpp
bool Aspose::Words::Drawing::Charts::ChartSeries::get_HasDataLabels() const
```


## Esempi



Mostra come abilitare e configurare le etichette dei dati per una serie di grafico.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Aggiungi un grafico a linee, quindi cancella la sua serie di dati demo per iniziare con un grafico pulito,
// e quindi imposta un titolo.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Line, 500, 300);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();
chart->get_Series()->Clear();
chart->get_Title()->set_Text(u"Monthly sales report");

// Inserisci una serie di grafico personalizzata con i mesi come categorie per l'asse X,
// e gli importi decimali corrispondenti per l'asse Y.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series = chart->get_Series()->Add(u"Revenue", System::MakeArray<System::String>({u"January", u"February", u"March"}), System::MakeArray<double>({25.611, 21.439, 33.750}));

// Abilita le etichette dei dati, quindi applica un formato numerico personalizzato per i valori visualizzati nelle etichette dei dati.
// Questo formato tratterà i valori decimali visualizzati come milioni di dollari statunitensi.
series->set_HasDataLabels(true);
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartDataLabelCollection> dataLabels = series->get_DataLabels();
dataLabels->set_ShowValue(true);
dataLabels->get_NumberFormat()->set_FormatCode(u"\"US$\" #,##0.000\"M\"");
dataLabels->get_Font()->set_Size(12);

doc->Save(get_ArtifactsDir() + u"Charts.DataLabelNumberFormat.docx");
```

## Vedi anche

* Class [ChartSeries](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
