---
title: "Aspose::Words::Drawing::Charts::ChartXValue::FromDouble metodo"
linktitle: "FromDouble"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Drawing::Charts::ChartXValue::FromDouble metodo. Crea un'istanza di ChartXValue del tipo Double in C++."
type: docs
weight: 2000
url: /it/cpp/aspose.words.drawing.charts/chartxvalue/fromdouble/
---
## ChartXValue::FromDouble method


Crea un'istanza di [ChartXValue](../) del tipo [Double](../../chartxvaluetype/).

```cpp
static System::SharedPtr<Aspose::Words::Drawing::Charts::ChartXValue> Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(double value)
```


## Esempi



Mostra come popolare le serie del grafico con i dati.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 432, 252);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series1 = chart->get_Series()->idx_get(0);

// Cancella i valori X e Y della prima serie.
series1->ClearValues();

// Popola la serie con i dati.
series1->Add(Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(3), Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(10), 10);
series1->Add(Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(5), Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(5));
series1->Add(Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(7), Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(11));
series1->Add(Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(9));

System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series2 = chart->get_Series()->idx_get(1);
// Cancella i valori X e Y della seconda serie.
series2->Clear();

// Popola la serie con i dati.
series2->Add(Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(2), Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(4));
series2->Add(Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(4), Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(7));
series2->Add(Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(6), Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(14));
series2->Add(Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(8), Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(7));

doc->Save(get_ArtifactsDir() + u"Charts.PopulateChartWithData.docx");
```

## Vedi anche

* Class [ChartXValue](../)
* Class [ChartXValue](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
