---
title: "Aspose::Words::Drawing::Charts::ChartNumberFormat class"
linktitle: "ChartNumberFormat"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Drawing::Charts::ChartNumberFormat class. Rappresenta la formattazione numerica dell'elemento padre. Per saperne di più, visita l'articolo della documentazione in C++."
type: docs
weight: 15000
url: /it/cpp/aspose.words.drawing.charts/chartnumberformat/
---
## ChartNumberFormat class


Rappresenta la formattazione numerica dell'elemento genitore. Per saperne di più, visita l'articolo di documentazione [Working with Charts](https://docs.aspose.com/words/cpp/working-with-charts/).

```cpp
class ChartNumberFormat : public System::Object
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [get_FormatCode](./get_formatcode/)() | Ottiene o imposta il codice di formato applicato a un'etichetta dati. |
| [get_IsLinkedToSource](./get_islinkedtosource/)() | Specifica se il codice di formato è collegato a una cella di origine. Il valore predefinito è true. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_FormatCode](./set_formatcode/)(const System::String\&) | Impostatore per [Aspose::Words::Drawing::Charts::ChartNumberFormat::get_FormatCode](./get_formatcode/). |
| [set_IsLinkedToSource](./set_islinkedtosource/)(bool) | Impostatore per [Aspose::Words::Drawing::Charts::ChartNumberFormat::get_IsLinkedToSource](./get_islinkedtosource/). |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
