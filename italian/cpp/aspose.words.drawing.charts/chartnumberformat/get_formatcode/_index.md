---
title: "Aspose::Words::Drawing::Charts::ChartNumberFormat::get_FormatCode metodo"
linktitle: "get_FormatCode"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Drawing::Charts::ChartNumberFormat::get_FormatCode metodo. Ottiene o imposta il codice di formato applicato a un'etichetta dati in C++."
type: docs
weight: 2000
url: /it/cpp/aspose.words.drawing.charts/chartnumberformat/get_formatcode/
---
## ChartNumberFormat::get_FormatCode method


Ottiene o imposta il codice di formato applicato a un'etichetta dati.

```cpp
System::String Aspose::Words::Drawing::Charts::ChartNumberFormat::get_FormatCode()
```

## Note


La formattazione dei numeri è usata per modificare il modo in cui un valore appare nell'etichetta dati e può essere utilizzata in modi molto creativi. Gli esempi di formati numerici:

Numero - "#,##0.00"

Valuta - "\"\$\\"#,##0.00"

Ora - "[$-x-systime]h:mm:ss AM/PM"

Data - "d/mm/yyyy"

Percentuale - "0.00%"

Frazione - "# ?/?"

Scientifico - "0.00E+00"

Testo - "@"

Contabilità - "_-\"\$\\"* #,##0.00_-;-\"\$\\"* #,##0.00_-;_-\"\$\\"* \"-\\"??_-;_-@_-"

Personalizzato con colore - "[Red]-#,##0.0"

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


Mostra come impostare la formattazione per i valori del grafico.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 500, 300);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();

// Cancella la serie di dati demo del grafico per iniziare con un grafico pulito.
chart->get_Series()->Clear();

// Aggiungi una serie personalizzata al grafico con categorie per l'asse X,
// e grandi valori numerici rispettivi per l'asse Y.
chart->get_Series()->Add(u"Aspose Test Series", System::MakeArray<System::String>({u"Word", u"PDF", u"Excel", u"GoogleDocs", u"Note"}), System::MakeArray<double>({1900000, 850000, 2100000, 600000, 1500000}));

// Imposta il formato numerico delle etichette dei tick dell'asse Y in modo da non raggruppare le cifre con le virgole.
chart->get_AxisY()->get_NumberFormat()->set_FormatCode(u"#,##0");

// Questa flag può sovrascrivere il valore sopra e prelevare il formato numerico dalla cella di origine.
ASSERT_FALSE(chart->get_AxisY()->get_NumberFormat()->get_IsLinkedToSource());

doc->Save(get_ArtifactsDir() + u"Charts.SetNumberFormatToChartAxis.docx");
```

## Vedi anche

* Class [ChartNumberFormat](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
