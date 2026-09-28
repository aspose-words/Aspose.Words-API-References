---
title: "Aspose::Words::Drawing::Charts::ChartSeries::Insert метод"
linktitle: "Insert"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Drawing::Charts::ChartSeries::Insert. Вставляет указанное значение X в серию диаграммы в указанном индексе. Если серия поддерживает значения Y и размеры пузырей, они будут пустыми для значения X в C++."
type: docs
weight: 13500
url: /ru/cpp/aspose.words.drawing.charts/chartseries/insert/
---
## ChartSeries::Insert(int32_t, const System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartXValue\>\&) method


Вставляет указанное значение X в серию диаграммы в указанный индекс. Если серия поддерживает значения Y и размеры пузырей, они будут пустыми для значения X.

```cpp
void Aspose::Words::Drawing::Charts::ChartSeries::Insert(int32_t index, const System::SharedPtr<Aspose::Words::Drawing::Charts::ChartXValue> &xValue)
```


## Примеры



Показывает, как вставить данные в серию диаграммы.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Line, 432, 252);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series1 = chart->get_Series()->idx_get(0);

// Очистить значения X и Y первой серии.
series1->ClearValues();
// Заполнить серию данными.
series1->Insert(0, Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(3));
series1->Insert(1, Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(3), Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(10));
series1->Insert(2, Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(3), Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(10));
series1->Insert(3, Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(3), Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(10), 10);

doc->Save(get_ArtifactsDir() + u"Charts.PopulateChartWithData.docx");
```

## См. также

* Class [ChartXValue](../../chartxvalue/)
* Class [ChartSeries](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
## ChartSeries::Insert(int32_t, const System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartXValue\>\&, const System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartYValue\>\&) method


Вставляет указанные значения X и Y в серию диаграммы в указанный индекс.

```cpp
void Aspose::Words::Drawing::Charts::ChartSeries::Insert(int32_t index, const System::SharedPtr<Aspose::Words::Drawing::Charts::ChartXValue> &xValue, const System::SharedPtr<Aspose::Words::Drawing::Charts::ChartYValue> &yValue)
```


## Примеры



Показывает, как вставить данные в серию диаграммы.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Line, 432, 252);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series1 = chart->get_Series()->idx_get(0);

// Очистить значения X и Y первой серии.
series1->ClearValues();
// Заполнить серию данными.
series1->Insert(0, Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(3));
series1->Insert(1, Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(3), Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(10));
series1->Insert(2, Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(3), Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(10));
series1->Insert(3, Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(3), Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(10), 10);

doc->Save(get_ArtifactsDir() + u"Charts.PopulateChartWithData.docx");
```

## См. также

* Class [ChartXValue](../../chartxvalue/)
* Class [ChartYValue](../../chartyvalue/)
* Class [ChartSeries](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
## ChartSeries::Insert(int32_t, const System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartXValue\>\&, const System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartYValue\>\&, double) method


Вставляет указанные значение X, значение Y и размер пузыря в серию диаграммы в указанный индекс.

```cpp
void Aspose::Words::Drawing::Charts::ChartSeries::Insert(int32_t index, const System::SharedPtr<Aspose::Words::Drawing::Charts::ChartXValue> &xValue, const System::SharedPtr<Aspose::Words::Drawing::Charts::ChartYValue> &yValue, double bubbleSize)
```


## Примеры



Показывает, как вставить данные в серию диаграммы.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Line, 432, 252);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series1 = chart->get_Series()->idx_get(0);

// Очистить значения X и Y первой серии.
series1->ClearValues();
// Заполнить серию данными.
series1->Insert(0, Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(3));
series1->Insert(1, Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(3), Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(10));
series1->Insert(2, Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(3), Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(10));
series1->Insert(3, Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(3), Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(10), 10);

doc->Save(get_ArtifactsDir() + u"Charts.PopulateChartWithData.docx");
```

## См. также

* Class [ChartXValue](../../chartxvalue/)
* Class [ChartYValue](../../chartyvalue/)
* Class [ChartSeries](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
