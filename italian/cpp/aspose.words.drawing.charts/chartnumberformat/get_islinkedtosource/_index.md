---
title: "Aspose::Words::Drawing::Charts::ChartNumberFormat::get_IsLinkedToSource metodo"
linktitle: "get_IsLinkedToSource"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Drawing::Charts::ChartNumberFormat::get_IsLinkedToSource metodo. Specifica se il codice di formato è collegato a una cella di origine. Il valore predefinito è true in C++."
type: docs
weight: 3000
url: /it/cpp/aspose.words.drawing.charts/chartnumberformat/get_islinkedtosource/
---
## ChartNumberFormat::get_IsLinkedToSource method


Specifica se il codice di formato è collegato a una cella di origine. Il valore predefinito è true.

```cpp
bool Aspose::Words::Drawing::Charts::ChartNumberFormat::get_IsLinkedToSource()
```


## Esempi



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
