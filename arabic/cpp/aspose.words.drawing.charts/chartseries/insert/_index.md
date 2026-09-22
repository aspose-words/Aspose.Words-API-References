---
title: "طريقة Aspose::Words::Drawing::Charts::ChartSeries::Insert"
linktitle: "Insert"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Drawing::Charts::ChartSeries::Insert. تُدرج قيمة X المحددة في سلسلة المخطط عند الفهرس المحدد. إذا كانت السلسلة تدعم قيم Y وأحجام الفقاعات، فستكون فارغة لقيمة X في C++."
type: docs
weight: 13500
url: /ar/cpp/aspose.words.drawing.charts/chartseries/insert/
---
## ChartSeries::Insert(int32_t, const System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartXValue\>\&) method


يدرج قيمة X المحددة في السلسلة البيانية عند الفهرس المحدد. إذا كانت السلسلة تدعم قيم Y وأحجام الفقاعات، فستكون فارغة بالنسبة لقيمة X.

```cpp
void Aspose::Words::Drawing::Charts::ChartSeries::Insert(int32_t index, const System::SharedPtr<Aspose::Words::Drawing::Charts::ChartXValue> &xValue)
```


## أمثلة



يعرض كيفية إدراج البيانات في سلسلة مخطط.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Line, 432, 252);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series1 = chart->get_Series()->idx_get(0);

// امسح قيم X و Y للسلسلة الأولى.
series1->ClearValues();
// املأ السلسلة بالبيانات.
series1->Insert(0, Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(3));
series1->Insert(1, Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(3), Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(10));
series1->Insert(2, Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(3), Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(10));
series1->Insert(3, Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(3), Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(10), 10);

doc->Save(get_ArtifactsDir() + u"Charts.PopulateChartWithData.docx");
```

## انظر أيضًا

* Class [ChartXValue](../../chartxvalue/)
* Class [ChartSeries](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
## ChartSeries::Insert(int32_t, const System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartXValue\>\&, const System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartYValue\>\&) method


يدرج قيم X و Y المحددة في السلسلة البيانية عند الفهرس المحدد.

```cpp
void Aspose::Words::Drawing::Charts::ChartSeries::Insert(int32_t index, const System::SharedPtr<Aspose::Words::Drawing::Charts::ChartXValue> &xValue, const System::SharedPtr<Aspose::Words::Drawing::Charts::ChartYValue> &yValue)
```


## أمثلة



يعرض كيفية إدراج البيانات في سلسلة مخطط.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Line, 432, 252);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series1 = chart->get_Series()->idx_get(0);

// امسح قيم X و Y للسلسلة الأولى.
series1->ClearValues();
// املأ السلسلة بالبيانات.
series1->Insert(0, Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(3));
series1->Insert(1, Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(3), Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(10));
series1->Insert(2, Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(3), Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(10));
series1->Insert(3, Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(3), Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(10), 10);

doc->Save(get_ArtifactsDir() + u"Charts.PopulateChartWithData.docx");
```

## انظر أيضًا

* Class [ChartXValue](../../chartxvalue/)
* Class [ChartYValue](../../chartyvalue/)
* Class [ChartSeries](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
## ChartSeries::Insert(int32_t, const System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartXValue\>\&, const System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartYValue\>\&, double) method


يدرج قيمة X المحددة، وقيمة Y، وحجم الفقاعة في السلسلة البيانية عند الفهرس المحدد.

```cpp
void Aspose::Words::Drawing::Charts::ChartSeries::Insert(int32_t index, const System::SharedPtr<Aspose::Words::Drawing::Charts::ChartXValue> &xValue, const System::SharedPtr<Aspose::Words::Drawing::Charts::ChartYValue> &yValue, double bubbleSize)
```


## أمثلة



يعرض كيفية إدراج البيانات في سلسلة مخطط.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Line, 432, 252);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series1 = chart->get_Series()->idx_get(0);

// امسح قيم X و Y للسلسلة الأولى.
series1->ClearValues();
// املأ السلسلة بالبيانات.
series1->Insert(0, Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(3));
series1->Insert(1, Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(3), Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(10));
series1->Insert(2, Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(3), Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(10));
series1->Insert(3, Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(3), Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(10), 10);

doc->Save(get_ArtifactsDir() + u"Charts.PopulateChartWithData.docx");
```

## انظر أيضًا

* Class [ChartXValue](../../chartxvalue/)
* Class [ChartYValue](../../chartyvalue/)
* Class [ChartSeries](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
