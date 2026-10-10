---
title: "Aspose::Words::Drawing::Charts::ChartSeries::Remove method"
linktitle: "Rimuovi"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Drawing::Charts::ChartSeries::Remove method. Rimuove il valore X, il valore Y e la dimensione della bolla, se supportati, dalla serie del grafico all'indice specificato. Anche il punto dati corrispondente e l'etichetta dei dati vengono rimossi in C++."
type: docs
weight: 14500
url: /it/cpp/aspose.words.drawing.charts/chartseries/remove/
---
## ChartSeries::Remove method


Rimuove il valore X, il valore Y e la dimensione della bolla, se supportati, dalla serie di grafico all'indice specificato. Anche il punto dati corrispondente e l'etichetta dati vengono rimossi.

```cpp
void Aspose::Words::Drawing::Charts::ChartSeries::Remove(int32_t index)
```


## Esempi



Mostra come aggiungere/rimuovere valori dei dati del grafico.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>();

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 432, 252);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> department1Series = chart->get_Series()->idx_get(0);
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> department2Series = chart->get_Series()->idx_get(1);

// Rimuovi il primo valore in entrambe le serie.
department1Series->Remove(0);
department2Series->Remove(0);

// Aggiungi nuovi valori a entrambe le serie.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartXValue> newXCategory = Aspose::Words::Drawing::Charts::ChartXValue::FromString(u"Q1, 2023");
department1Series->Add(newXCategory, Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(10.3));
department2Series->Add(newXCategory, Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(5.7));

doc->Save(get_ArtifactsDir() + u"Charts.ChartDataValues.docx");
```

## Vedi anche

* Class [ChartSeries](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
