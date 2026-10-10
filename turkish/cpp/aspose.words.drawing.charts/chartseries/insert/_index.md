---
title: "Aspose::Words::Drawing::Charts::ChartSeries::Insert metodu"
linktitle: "Insert"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::Charts::ChartSeries::Insert method. Belirtilen X değerini belirtilen indekste grafik serisine ekler. Seri Y değerlerini ve balon boyutlarını destekliyorsa, C++'ta X değeri için bunlar boş olacaktır."
type: docs
weight: 13500
url: /tr/cpp/aspose.words.drawing.charts/chartseries/insert/
---
## ChartSeries::Insert(int32_t, const System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartXValue\>\&) method


Belirtilen X değerini belirtilen indekste grafik serisine ekler. Seri Y değerlerini ve baloncuk boyutlarını destekliyorsa, X değeri için bunlar boş olur.

```cpp
void Aspose::Words::Drawing::Charts::ChartSeries::Insert(int32_t index, const System::SharedPtr<Aspose::Words::Drawing::Charts::ChartXValue> &xValue)
```


## Örnekler



Bir grafik serisine veri eklemenin nasıl yapılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Line, 432, 252);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series1 = chart->get_Series()->idx_get(0);

// İlk serinin X ve Y değerlerini temizle.
series1->ClearValues();
// Seriyi veriyle doldur.
series1->Insert(0, Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(3));
series1->Insert(1, Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(3), Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(10));
series1->Insert(2, Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(3), Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(10));
series1->Insert(3, Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(3), Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(10), 10);

doc->Save(get_ArtifactsDir() + u"Charts.PopulateChartWithData.docx");
```

## Ayrıca Bakınız

* Class [ChartXValue](../../chartxvalue/)
* Class [ChartSeries](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
## ChartSeries::Insert(int32_t, const System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartXValue\>\&, const System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartYValue\>\&) method


Belirtilen X ve Y değerlerini belirtilen indekste grafik serisine ekler.

```cpp
void Aspose::Words::Drawing::Charts::ChartSeries::Insert(int32_t index, const System::SharedPtr<Aspose::Words::Drawing::Charts::ChartXValue> &xValue, const System::SharedPtr<Aspose::Words::Drawing::Charts::ChartYValue> &yValue)
```


## Örnekler



Bir grafik serisine veri eklemenin nasıl yapılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Line, 432, 252);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series1 = chart->get_Series()->idx_get(0);

// İlk serinin X ve Y değerlerini temizle.
series1->ClearValues();
// Seriyi veriyle doldur.
series1->Insert(0, Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(3));
series1->Insert(1, Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(3), Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(10));
series1->Insert(2, Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(3), Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(10));
series1->Insert(3, Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(3), Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(10), 10);

doc->Save(get_ArtifactsDir() + u"Charts.PopulateChartWithData.docx");
```

## Ayrıca Bakınız

* Class [ChartXValue](../../chartxvalue/)
* Class [ChartYValue](../../chartyvalue/)
* Class [ChartSeries](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
## ChartSeries::Insert(int32_t, const System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartXValue\>\&, const System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartYValue\>\&, double) method


Belirtilen X değeri, Y değeri ve baloncuk boyutunu belirtilen indekste grafik serisine ekler.

```cpp
void Aspose::Words::Drawing::Charts::ChartSeries::Insert(int32_t index, const System::SharedPtr<Aspose::Words::Drawing::Charts::ChartXValue> &xValue, const System::SharedPtr<Aspose::Words::Drawing::Charts::ChartYValue> &yValue, double bubbleSize)
```


## Örnekler



Bir grafik serisine veri eklemenin nasıl yapılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Line, 432, 252);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series1 = chart->get_Series()->idx_get(0);

// İlk serinin X ve Y değerlerini temizle.
series1->ClearValues();
// Seriyi veriyle doldur.
series1->Insert(0, Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(3));
series1->Insert(1, Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(3), Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(10));
series1->Insert(2, Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(3), Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(10));
series1->Insert(3, Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(3), Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(10), 10);

doc->Save(get_ArtifactsDir() + u"Charts.PopulateChartWithData.docx");
```

## Ayrıca Bakınız

* Class [ChartXValue](../../chartxvalue/)
* Class [ChartYValue](../../chartyvalue/)
* Class [ChartSeries](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
