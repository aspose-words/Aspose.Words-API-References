---
title: "Aspose::Words::Drawing::Charts::ChartDataLabelPosition enum"
linktitle: "ChartDataLabelPosition"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Drawing::Charts::ChartDataLabelPosition enum. Specifica la posizione di un'etichetta dati del grafico in C++."
type: docs
weight: 27334
url: /it/cpp/aspose.words.drawing.charts/chartdatalabelposition/
---
## ChartDataLabelPosition enum


Specifica la posizione per un'etichetta dati del grafico.

```cpp
enum class ChartDataLabelPosition
```

### Valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Centro | 0 | Specifica che un'etichetta dati deve essere visualizzata centrata su un marcatore dati. |
| Sinistra | 1 | Specifica che un'etichetta dati deve essere visualizzata a sinistra di un marcatore dati. |
| Destra | 2 | Specifica che un'etichetta dati deve essere visualizzata a destra di un marcatore dati. |
| Sopra | 3 | Specifica che un'etichetta dati deve essere visualizzata sopra un marcatore dati. |
| Sotto | 4 | Specifica che un'etichetta dati deve essere visualizzata sotto un marcatore dati. |
| InsideBase | 5 | Specifica che un'etichetta dati deve essere visualizzata all'interno della base di un marcatore dati. |
| InsideEnd | 6 | Specifica che un'etichetta dati deve essere visualizzata all'interno della fine di un marcatore dati. |
| OutsideEnd | 7 | Specifica che un'etichetta dati deve essere visualizzata al di fuori dell'estremità di un marcatore dati. |
| BestFit | 8 | Specifica che un'etichetta dati deve essere visualizzata nella posizione più appropriata. |


## Esempi



Mostra come impostare la posizione dell'etichetta dati.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Inserisci un grafico a colonne.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 432, 252);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeriesCollection> seriesColl = chart->get_Series();

// Elimina la serie generata di default.
seriesColl->Clear();

// Aggiungi serie.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series = seriesColl->Add(u"Series 1", System::MakeArray<System::String>({u"Category 1", u"Category 2", u"Category 3"}), System::MakeArray<double>({4, 5, 6}));

// Mostra le etichette dati e imposta il colore del carattere.
series->set_HasDataLabels(true);
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartDataLabelCollection> dataLabels = series->get_DataLabels();
dataLabels->set_ShowValue(true);
dataLabels->get_Font()->set_Color(System::Drawing::Color::get_White());

// Imposta la posizione dell'etichetta dati.
dataLabels->set_Position(Aspose::Words::Drawing::Charts::ChartDataLabelPosition::InsideBase);
dataLabels->idx_get(0)->set_Position(Aspose::Words::Drawing::Charts::ChartDataLabelPosition::OutsideEnd);
dataLabels->idx_get(0)->get_Font()->set_Color(System::Drawing::Color::get_DarkRed());

doc->Save(get_ArtifactsDir() + u"Charts.LabelPosition.docx");
```

## Vedi anche

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
