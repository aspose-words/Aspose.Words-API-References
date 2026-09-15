---
title: "Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_FirstSliceAngle طريقة"
linktitle: "get_FirstSliceAngle"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_FirstSliceAngle طريقة. يحصل على أو يضبط الزاوية، بالدرجات، للقطعة الأولى من مخطط الفطيرة الأصل في C++."
type: docs
weight: 7000
url: /ar/cpp/aspose.words.drawing.charts/chartseriesgroup/get_firstsliceangle/
---
## ChartSeriesGroup::get_FirstSliceAngle method


يحصل أو يعيّن الزاوية، بالدرجات، للقطعة الأولى في مخطط الفطيرة الأب.

```cpp
int32_t Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_FirstSliceAngle()
```

## ملاحظات


ينطبق على مجموعات السلاسل من أنواع [Pie](../../chartseriestype/)، [Pie3D](../../chartseriestype/) و [Doughnut](../../chartseriestype/).

النطاق المقبول للقيم هو من 0 إلى 360 شاملًا. القيمة الافتراضية هي 0.

## أمثلة



يعرض كيفية إنشاء وتنسيق مخطط الدونات.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Doughnut, 400, 400);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();
// احذف السلسلة التي تم إنشاؤها افتراضيًا.
chart->get_Series()->Clear();

auto categories = System::MakeArray<System::String>({u"Category 1", u"Category 2", u"Category 3"});
chart->get_Series()->Add(u"Series 1", categories, System::MakeArray<double>({4, 2, 5}));

// قم بتنسيق مخطط الدونات.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeriesGroup> seriesGroup = chart->get_SeriesGroups()->idx_get(0);
seriesGroup->set_DoughnutHoleSize(10);
seriesGroup->set_FirstSliceAngle(270);

doc->Save(get_ArtifactsDir() + u"Charts.DoughnutChart.docx");
```

## انظر أيضًا

* Class [ChartSeriesGroup](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
