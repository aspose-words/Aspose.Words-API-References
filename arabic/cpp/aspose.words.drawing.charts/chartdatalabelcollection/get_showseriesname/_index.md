---
title: "طريقة Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_ShowSeriesName"
linktitle: "get_ShowSeriesName"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_ShowSeriesName. تُرجع أو تُعيّن قيمة منطقية لتحديد سلوك عرض اسم السلسلة لتسميات البيانات للسلسلة بأكملها. true لإظهار اسم السلسلة؛ false لإخفائه. القيمة الافتراضية هي false في C++."
type: docs
weight: 13000
url: /ar/cpp/aspose.words.drawing.charts/chartdatalabelcollection/get_showseriesname/
---
## ChartDataLabelCollection::get_ShowSeriesName method


يعيد أو يضبط قيمة منطقية لتحديد سلوك عرض اسم السلسلة لتسميات البيانات للسلسلة بأكملها. **true** لإظهار اسم السلسلة؛ **false** لإخفائه. بشكل افتراضي **false**.

```cpp
bool Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_ShowSeriesName()
```


## أمثلة



يعرض كيفية العمل مع تسميات البيانات في مخطط الفقاعات.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Bubble, 500, 300)->get_Chart();

// امسح سلسلة بيانات العرض التجريبية للمخطط للبدء بمخطط نظيف.
chart->get_Series()->Clear();

// أضف سلسلة مخصصة بإحداثيات X/Y وقطر كل فقاعة.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series = chart->get_Series()->Add(u"Aspose Test Series", System::MakeArray<double>({2.9, 3.5, 1.1, 4.0, 4.0}), System::MakeArray<double>({1.9, 8.5, 2.1, 6.0, 1.5}), System::MakeArray<double>({9.0, 4.5, 2.5, 8.0, 5.0}));

// فعّل تسميات البيانات، ثم عدّل مظهرها.
series->set_HasDataLabels(true);
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartDataLabelCollection> dataLabels = series->get_DataLabels();
dataLabels->set_ShowBubbleSize(true);
dataLabels->set_ShowCategoryName(true);
dataLabels->set_ShowSeriesName(true);
dataLabels->set_Separator(u" & ");

doc->Save(get_ArtifactsDir() + u"Charts.DataLabelsBubbleChart.docx");
```

## انظر أيضًا

* Class [ChartDataLabelCollection](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
