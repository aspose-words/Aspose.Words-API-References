---
title: "طريقة Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_BubbleScale. يحصل على أو يضبط حجم الفقاعات كنسبة مئوية من حجمها الافتراضي في C++."
linktitle: "ينطبق فقط على مجموعات السلاسل من نوعي [Bubble](../../chartseriestype/) و[Bubble3D](../../chartseriestype/)."
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "نطاق القيم المقبولة هو من 0 إلى 300 شاملًا. القيمة الافتراضية هي 100."
type: docs
weight: 5000
url: /ar/cpp/aspose.words.drawing.charts/chartseriesgroup/get_bubblescale/
---
## ChartSeriesGroup::get_BubbleScale method


يحصل أو يعيّن حجم الفقاعات كنسبة مئوية من حجمها الافتراضي.

```cpp
int32_t Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_BubbleScale()
```

## ملاحظات


أظهر كيفية ضبط حجم الفقاعات.

أدرج مخطط فقاعة ثلاثي الأبعاد.

## أمثلة



اضبط مقياس الفقاعات إلى 200%.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// طريقة Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_AxisGroup
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Bubble3D, 450, 250);
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeriesGroup> seriesGroup = shape->get_Chart()->get_SeriesGroups()->idx_get(0);

// get_AxisGroup
seriesGroup->set_BubbleScale(200);

doc->Save(get_ArtifactsDir() + u"Charts.BubbleScale.docx");
```

## انظر أيضًا

* Class [ChartSeriesGroup](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
