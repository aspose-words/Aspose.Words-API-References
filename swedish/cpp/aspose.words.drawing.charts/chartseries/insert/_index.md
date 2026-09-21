---
title: "Aspose::Words::Drawing::Charts::ChartSeries::Insert method"
linktitle: "Infoga"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Drawing::Charts::ChartSeries::Insert method. Infogar det angivna X‑värdet i diagramserien på det angivna indexet. Om serien stödjer Y‑värden och bubbelformer kommer de att vara tomma för X‑värdet i C++."
type: docs
weight: 13500
url: /sv/cpp/aspose.words.drawing.charts/chartseries/insert/
---
## ChartSeries::Insert(int32_t, const System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartXValue\>\&) method


Infogar det angivna X‑värdet i diagramserien på det angivna indexet. Om serien stöder Y‑värden och bubbla‑storlekar kommer de att vara tomma för X‑värdet.

```cpp
void Aspose::Words::Drawing::Charts::ChartSeries::Insert(int32_t index, const System::SharedPtr<Aspose::Words::Drawing::Charts::ChartXValue> &xValue)
```


## Exempel



Visar hur man infogar data i en diagramserie.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Line, 432, 252);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series1 = chart->get_Series()->idx_get(0);

// Rensa X‑ och Y‑värdena i den första serien.
series1->ClearValues();
// Fyll serien med data.
series1->Insert(0, Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(3));
series1->Insert(1, Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(3), Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(10));
series1->Insert(2, Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(3), Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(10));
series1->Insert(3, Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(3), Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(10), 10);

doc->Save(get_ArtifactsDir() + u"Charts.PopulateChartWithData.docx");
```

## Se även

* Class [ChartXValue](../../chartxvalue/)
* Class [ChartSeries](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
## ChartSeries::Insert(int32_t, const System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartXValue\>\&, const System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartYValue\>\&) method


Infogar de angivna X‑ och Y‑värdena i diagramserien på det angivna indexet.

```cpp
void Aspose::Words::Drawing::Charts::ChartSeries::Insert(int32_t index, const System::SharedPtr<Aspose::Words::Drawing::Charts::ChartXValue> &xValue, const System::SharedPtr<Aspose::Words::Drawing::Charts::ChartYValue> &yValue)
```


## Exempel



Visar hur man infogar data i en diagramserie.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Line, 432, 252);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series1 = chart->get_Series()->idx_get(0);

// Rensa X‑ och Y‑värdena i den första serien.
series1->ClearValues();
// Fyll serien med data.
series1->Insert(0, Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(3));
series1->Insert(1, Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(3), Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(10));
series1->Insert(2, Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(3), Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(10));
series1->Insert(3, Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(3), Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(10), 10);

doc->Save(get_ArtifactsDir() + u"Charts.PopulateChartWithData.docx");
```

## Se även

* Class [ChartXValue](../../chartxvalue/)
* Class [ChartYValue](../../chartyvalue/)
* Class [ChartSeries](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
## ChartSeries::Insert(int32_t, const System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartXValue\>\&, const System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartYValue\>\&, double) method


Infogar det angivna X‑värdet, Y‑värdet och bubbla‑storleken i diagramserien på det angivna indexet.

```cpp
void Aspose::Words::Drawing::Charts::ChartSeries::Insert(int32_t index, const System::SharedPtr<Aspose::Words::Drawing::Charts::ChartXValue> &xValue, const System::SharedPtr<Aspose::Words::Drawing::Charts::ChartYValue> &yValue, double bubbleSize)
```


## Exempel



Visar hur man infogar data i en diagramserie.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Line, 432, 252);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series1 = chart->get_Series()->idx_get(0);

// Rensa X‑ och Y‑värdena i den första serien.
series1->ClearValues();
// Fyll serien med data.
series1->Insert(0, Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(3));
series1->Insert(1, Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(3), Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(10));
series1->Insert(2, Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(3), Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(10));
series1->Insert(3, Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(3), Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(10), 10);

doc->Save(get_ArtifactsDir() + u"Charts.PopulateChartWithData.docx");
```

## Se även

* Class [ChartXValue](../../chartxvalue/)
* Class [ChartYValue](../../chartyvalue/)
* Class [ChartSeries](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
