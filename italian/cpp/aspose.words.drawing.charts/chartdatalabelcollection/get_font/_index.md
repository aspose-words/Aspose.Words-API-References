---
title: "Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_Font metodo"
linktitle: "get_Font"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_Font metodo. Fornisce l'accesso alla formattazione del carattere delle etichette dei dati dell'intera serie in C++."
type: docs
weight: 4000
url: /it/cpp/aspose.words.drawing.charts/chartdatalabelcollection/get_font/
---
## ChartDataLabelCollection::get_Font method


Fornisce l'accesso alla formattazione del carattere delle etichette dati dell'intera serie.

```cpp
System::SharedPtr<Aspose::Words::Font> Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_Font()
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

* Class [Font](../../../aspose.words/font/)
* Class [ChartDataLabelCollection](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
