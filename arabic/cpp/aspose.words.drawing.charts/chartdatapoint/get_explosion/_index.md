---
title: "Aspose::Words::Drawing::Charts::ChartDataPoint::get_Explosion طريقة"
linktitle: "get_Explosion"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Drawing::Charts::ChartDataPoint::get_Explosion طريقة. يحدد مقدار تحريك نقطة البيانات من مركز الفطيرة. يمكن أن يكون سالبًا، السالب يعني أن الخاصية غير مضبوطة ولا يجب تطبيق أي انفجار. يُطبق فقط على مخططات الفطيرة في C++."
type: docs
weight: 4000
url: /ar/cpp/aspose.words.drawing.charts/chartdatapoint/get_explosion/
---
## ChartDataPoint::get_Explosion method


يحدد مقدار إزاحة نقطة البيانات من مركز الفطيرة. يمكن أن يكون سالبًا، السالب يعني أن الخاصية غير مضبوطة ولا يجب تطبيق أي انفجار. ينطبق فقط على مخططات الفطيرة.

```cpp
int32_t Aspose::Words::Drawing::Charts::ChartDataPoint::get_Explosion() override
```


## أمثلة



يوضح كيفية تحريك شرائح مخطط الفطيرة بعيدًا عن المركز.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Pie, 500, 350);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();

ASSERT_EQ(1, chart->get_Series()->get_Count());
ASSERT_EQ(u"Sales", chart->get_Series()->idx_get(0)->get_Name());

// \"Slices\" من مخطط الفطيرة قد تُنقل بعيدًا عن المركز بمسافة عبر خاصية Explosion لنقطة البيانات المعنية.
// أضف نقطة بيانات إلى الجزء الأول من مخطط الفطيرة وحركها بعيدًا عن المركز بمقدار 10 نقاط.
// Aspose.Words ينشئ نقاط البيانات تلقائيًا إذا لم تكن موجودة.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartDataPoint> dataPoint = chart->get_Series()->idx_get(0)->get_DataPoints()->idx_get(0);
dataPoint->set_Explosion(10);

// قم بإزاحة الجزء الثاني بمسافة أكبر.
dataPoint = chart->get_Series()->idx_get(0)->get_DataPoints()->idx_get(1);
dataPoint->set_Explosion(40);

doc->Save(get_ArtifactsDir() + u"Charts.PieChartExplosion.docx");
```

## انظر أيضًا

* Class [ChartDataPoint](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
