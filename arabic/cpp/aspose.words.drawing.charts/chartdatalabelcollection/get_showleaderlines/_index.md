---
title: "Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_ShowLeaderLines طريقة"
linktitle: "get_ShowLeaderLines"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_ShowLeaderLines طريقة. يسمح بتحديد ما إذا كان يجب إظهار خطوط القائد لتسميات البيانات للسلسلة بأكملها. القيمة الافتراضية هي false في C++."
type: docs
weight: 10000
url: /ar/cpp/aspose.words.drawing.charts/chartdatalabelcollection/get_showleaderlines/
---
## ChartDataLabelCollection::get_ShowLeaderLines method


يسمح بتحديد ما إذا كان يجب إظهار خطوط القائد لتسميات البيانات للسلسلة بأكملها. القيمة الافتراضية هي **false**.

```cpp
bool Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_ShowLeaderLines()
```

## ملاحظات


ينطبق على مخططات الفطيرة فقط. خطوط القائد تخلق اتصالًا بصريًا بين تسمية البيانات والنقطة البيانات المقابلة لها.

القيمة المحددة لهذا الخاصية يمكن تجاوزها لتسمية بيانات فردية باستخدام خاصية [ShowLeaderLines](../../chartdatalabel/get_showleaderlines/).

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
