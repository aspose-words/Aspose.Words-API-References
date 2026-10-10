---
title: "Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_ShowPercentage طريقة"
linktitle: "get_ShowPercentage"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_ShowPercentage طريقة. يسمح بتحديد ما إذا كان يجب عرض قيمة النسبة المئوية لتسميات البيانات للسلسلة بأكملها. القيمة الافتراضية هي false. ينطبق فقط على مخططات الفطيرة في C++."
type: docs
weight: 12000
url: /ar/cpp/aspose.words.drawing.charts/chartdatalabelcollection/get_showpercentage/
---
## ChartDataLabelCollection::get_ShowPercentage method


يسمح بتحديد ما إذا كان يجب عرض القيمة النسبية لتسميات البيانات للسلسلة بأكملها. القيمة الافتراضية هي **false**. ينطبق فقط على المخططات الدائرية.

```cpp
bool Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_ShowPercentage()
```


## أمثلة



يعرض كيفية العمل مع تسميات البيانات في مخطط الفطيرة.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Pie, 500, 300)->get_Chart();

// امسح سلسلة بيانات العرض التجريبية للمخطط للبدء بمخطط نظيف.
chart->get_Series()->Clear();

// أدرج سلسلة مخطط مخصصة باسم فئة لكل قطاع، وجدول ترددها.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series = chart->get_Series()->Add(u"Aspose Test Series", System::MakeArray<System::String>({u"Word", u"PDF", u"Excel"}), System::MakeArray<double>({2.7, 3.2, 0.8}));

// فعّل تسميات البيانات التي ستعرض النسبة المئوية والتردد لكل قطاع، وعدّل مظهرها.
series->set_HasDataLabels(true);
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartDataLabelCollection> dataLabels = series->get_DataLabels();
dataLabels->set_ShowLeaderLines(true);
dataLabels->set_ShowLegendKey(true);
dataLabels->set_ShowPercentage(true);
dataLabels->set_ShowValue(true);
dataLabels->set_Separator(u"; ");

doc->Save(get_ArtifactsDir() + u"Charts.DataLabelsPieChart.docx");
```

## انظر أيضًا

* Class [ChartDataLabelCollection](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
