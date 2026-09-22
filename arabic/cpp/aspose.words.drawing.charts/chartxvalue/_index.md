---
title: "فئة Aspose::Words::Drawing::Charts::ChartXValue"
linktitle: "ChartXValue"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "فئة Aspose::Words::Drawing::Charts::ChartXValue. تمثل قيمة X لسلسلة مخطط في C++."
type: docs
weight: 18200
url: /ar/cpp/aspose.words.drawing.charts/chartxvalue/
---
## ChartXValue class


يمثل قيمة X لسلسلة المخطط.

```cpp
class ChartXValue : public System::Object
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [Equals](./equals/)(System::SharedPtr\<System::Object\>) override | يحصل على علم يشير إلى ما إذا كان الكائن المحدد يساوي كائن قيمة X الحالي. |
| static [FromDateTime](./fromdatetime/)(System::DateTime) | ينشئ مثلاً من [ChartXValue](./) من النوع [DateTime](../chartxvaluetype/). |
| static [FromDouble](./fromdouble/)(double) | ينشئ مثلاً من [ChartXValue](./) من النوع [Double](../chartxvaluetype/). |
| static [FromMultilevelValue](./frommultilevelvalue/)(const System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartMultilevelValue\>\&) | ينشئ مثلاً من [ChartXValue](./) من النوع [Multilevel](../chartxvaluetype/). |
| static [FromString](./fromstring/)(const System::String\&) | ينشئ مثلاً من [ChartXValue](./) من النوع [String](../chartxvaluetype/). |
| static [FromTimeSpan](./fromtimespan/)(System::TimeSpan) | ينشئ مثلاً من [ChartXValue](./) من النوع [Time](../chartxvaluetype/). |
| [get_DateTimeValue](./get_datetimevalue/)() const | يحصل على قيمة التاريخ والوقت المخزنة. |
| [get_DoubleValue](./get_doublevalue/)() const | يحصل على القيمة الرقمية المخزنة. |
| [get_MultilevelValue](./get_multilevelvalue/)() const | يحصل على القيمة المتعددة المستويات المخزنة. |
| [get_StringValue](./get_stringvalue/)() const | يحصل على قيمة السلسلة المخزنة. |
| [get_TimeValue](./get_timevalue/)() const | يحصل على قيمة الوقت المخزنة. |
| [get_ValueType](./get_valuetype/)() const | يحصل على نوع قيمة X المخزنة في الكائن. |
| [GetHashCode](./gethashcode/)() const override | يحصل على رمز تجزئة لكائن قيمة X الحالي. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## ملاحظات


تحتوي هذه الفئة على عدد من الطرق الساكنة لإنشاء قيمة X من نوع معين. تسمح لك الخاصية [ValueType](./get_valuetype/) بتحديد نوع قيمة X الموجودة.

يجب أن تكون جميع قيم X غير الفارغة لسلسلة مخطط من نفس النوع [ChartXValueType](../chartxvaluetype/).

## أمثلة



يوضح كيفية ملء سلاسل المخطط بالبيانات.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 432, 252);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series1 = chart->get_Series()->idx_get(0);

// امسح قيم X و Y للسلسلة الأولى.
series1->ClearValues();

// املأ السلسلة بالبيانات.
series1->Add(Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(3), Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(10), 10);
series1->Add(Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(5), Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(5));
series1->Add(Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(7), Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(11));
series1->Add(Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(9));

System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series2 = chart->get_Series()->idx_get(1);
// امسح قيم X و Y للسلسلة الثانية.
series2->Clear();

// املأ السلسلة بالبيانات.
series2->Add(Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(2), Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(4));
series2->Add(Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(4), Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(7));
series2->Add(Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(6), Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(14));
series2->Add(Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(8), Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(7));

doc->Save(get_ArtifactsDir() + u"Charts.PopulateChartWithData.docx");
```

## انظر أيضًا

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
