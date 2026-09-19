---
title: "Aspose::Words::Drawing::Charts::ChartYValueCollection::get_FormatCode metodo"
linktitle: "get_FormatCode"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Drawing::Charts::ChartYValueCollection::get_FormatCode metodo. Ottiene o imposta il codice di formato applicato ai valori Y in C++."
type: docs
weight: 2500
url: /it/cpp/aspose.words.drawing.charts/chartyvaluecollection/get_formatcode/
---
## ChartYValueCollection::get_FormatCode method


Ottiene o imposta il codice di formato applicato ai valori Y.

```cpp
System::String Aspose::Words::Drawing::Charts::ChartYValueCollection::get_FormatCode()
```

## Note


La formattazione dei numeri è usata per modificare il modo in cui i valori appaiono nel grafico. Esempi di formati numerici:

Numero - "#,##0.00"

Valuta - "\"\$\\"#,##0.00"

Ora - "[$-x-systime]h:mm:ss AM/PM"

Data - "d/mm/yyyy"

Percentuale - "0.00%"

Frazione - "# ?/?"

Scientifico - "0.00E+00"

Contabilità - "_-\"\$\\"* #,##0.00_-;-\"\$\\"* #,##0.00_-;_-\"\$\\"* \"-\\"??_-;_-@_-"

Personalizzato con colore - "[Red]-#,##0.0"

## Esempi



Mostra come lavorare con il codice di formato dei dati del grafico.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Inserisci un grafico a bolle.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Bubble, 432, 252);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();

// Elimina la serie generata di default.
chart->get_Series()->Clear();

System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series = chart->get_Series()->Add(u"Series1", System::MakeArray<double>({1, 1.9, 2.45, 3}), System::MakeArray<double>({1, -0.9, 1.82, 0}), System::MakeArray<double>({2, 1.1, 2.95, 2}));

// Mostra le etichette dati.
series->set_HasDataLabels(true);
series->get_DataLabels()->set_ShowCategoryName(true);
series->get_DataLabels()->set_ShowValue(true);
series->get_DataLabels()->set_ShowBubbleSize(true);

// Imposta i codici di formato dei dati.
series->get_XValues()->set_FormatCode(u"#,##0.0#");
series->get_YValues()->set_FormatCode(u"#,##0.0#;[Red]\\-#,##0.0#");
series->get_BubbleSizes()->set_FormatCode(u"#,##0.0#");

doc->Save(get_ArtifactsDir() + u"Charts.FormatCode.docx");
```

## Vedi anche

* Class [ChartYValueCollection](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
