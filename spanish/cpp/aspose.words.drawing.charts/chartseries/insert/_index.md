---
title: "Método Aspose::Words::Drawing::Charts::ChartSeries::Insert"
linktitle: "Insert"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Drawing::Charts::ChartSeries::Insert. Inserta el valor X especificado en la serie del gráfico en el índice especificado. Si la serie admite valores Y y tamaños de burbuja, estarán vacíos para el valor X en C++."
type: docs
weight: 13500
url: /es/cpp/aspose.words.drawing.charts/chartseries/insert/
---
## ChartSeries::Insert(int32_t, const System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartXValue\>\&) method


Inserta el valor X especificado en la serie de gráfico en el índice indicado. Si la serie admite valores Y y tamaños de burbuja, estarán vacíos para el valor X.

```cpp
void Aspose::Words::Drawing::Charts::ChartSeries::Insert(int32_t index, const System::SharedPtr<Aspose::Words::Drawing::Charts::ChartXValue> &xValue)
```


## Ejemplos



Mostrar cómo insertar datos en una serie de gráfico.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Line, 432, 252);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series1 = chart->get_Series()->idx_get(0);

// Borra los valores X e Y de la primera serie.
series1->ClearValues();
// Rellena la serie con datos.
series1->Insert(0, Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(3));
series1->Insert(1, Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(3), Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(10));
series1->Insert(2, Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(3), Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(10));
series1->Insert(3, Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(3), Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(10), 10);

doc->Save(get_ArtifactsDir() + u"Charts.PopulateChartWithData.docx");
```

## Ver también

* Class [ChartXValue](../../chartxvalue/)
* Class [ChartSeries](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
## ChartSeries::Insert(int32_t, const System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartXValue\>\&, const System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartYValue\>\&) method


Inserta los valores X y Y especificados en la serie de gráfico en el índice indicado.

```cpp
void Aspose::Words::Drawing::Charts::ChartSeries::Insert(int32_t index, const System::SharedPtr<Aspose::Words::Drawing::Charts::ChartXValue> &xValue, const System::SharedPtr<Aspose::Words::Drawing::Charts::ChartYValue> &yValue)
```


## Ejemplos



Mostrar cómo insertar datos en una serie de gráfico.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Line, 432, 252);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series1 = chart->get_Series()->idx_get(0);

// Borra los valores X e Y de la primera serie.
series1->ClearValues();
// Rellena la serie con datos.
series1->Insert(0, Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(3));
series1->Insert(1, Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(3), Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(10));
series1->Insert(2, Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(3), Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(10));
series1->Insert(3, Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(3), Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(10), 10);

doc->Save(get_ArtifactsDir() + u"Charts.PopulateChartWithData.docx");
```

## Ver también

* Class [ChartXValue](../../chartxvalue/)
* Class [ChartYValue](../../chartyvalue/)
* Class [ChartSeries](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
## ChartSeries::Insert(int32_t, const System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartXValue\>\&, const System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartYValue\>\&, double) method


Inserta el valor X, el valor Y y el tamaño de burbuja especificados en la serie de gráfico en el índice indicado.

```cpp
void Aspose::Words::Drawing::Charts::ChartSeries::Insert(int32_t index, const System::SharedPtr<Aspose::Words::Drawing::Charts::ChartXValue> &xValue, const System::SharedPtr<Aspose::Words::Drawing::Charts::ChartYValue> &yValue, double bubbleSize)
```


## Ejemplos



Mostrar cómo insertar datos en una serie de gráfico.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Line, 432, 252);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series1 = chart->get_Series()->idx_get(0);

// Borra los valores X e Y de la primera serie.
series1->ClearValues();
// Rellena la serie con datos.
series1->Insert(0, Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(3));
series1->Insert(1, Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(3), Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(10));
series1->Insert(2, Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(3), Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(10));
series1->Insert(3, Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(3), Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(10), 10);

doc->Save(get_ArtifactsDir() + u"Charts.PopulateChartWithData.docx");
```

## Ver también

* Class [ChartXValue](../../chartxvalue/)
* Class [ChartYValue](../../chartyvalue/)
* Class [ChartSeries](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
