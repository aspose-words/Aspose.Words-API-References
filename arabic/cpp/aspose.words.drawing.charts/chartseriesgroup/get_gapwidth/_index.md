---
title: "Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_GapWidth طريقة"
linktitle: "get_GapWidth"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_GapWidth طريقة. يحصل أو يضبط نسبة عرض الفجوة بين عناصر المخطط في C++."
type: docs
weight: 8000
url: /ar/cpp/aspose.words.drawing.charts/chartseriesgroup/get_gapwidth/
---
## ChartSeriesGroup::get_GapWidth method


يحصل أو يعيّن نسبة عرض الفجوة بين عناصر المخطط.

```cpp
int32_t Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_GapWidth()
```

## ملاحظات


ينطبق فقط على مجموعات السلاسل لأنواع الشريط، العمود، فطيرة-الشريط، فطيرة-الفطيرة، المخطط التكراري، box&whisker، الشلال والقمع.

نطاق القيم المقبولة هو من 0 إلى 500 شاملًا. بالنسبة لمجموعات السلاسل القائمة على الشريط/العمود، تمثل الخاصية المسافة بين مجموعات الأشرطة كنسبة مئوية من عرضها. بالنسبة لمخططات فطيرة-فطيرة و شريط-فطيرة، تكون هذه هي المسافة بين الأقسام الأولية والثانوية للمخطط.

## أمثلة



إظهار كيفية تكوين عرض الفجوة والتداخل.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 450, 250);
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeriesGroup> seriesGroup = shape->get_Chart()->get_SeriesGroups()->idx_get(0);

// تعيين عرض الفجوة للعمود والتداخل.
seriesGroup->set_GapWidth(450);
seriesGroup->set_Overlap(-75);

doc->Save(get_ArtifactsDir() + u"Charts.ConfigureGapOverlap.docx");
```

## انظر أيضًا

* Class [ChartSeriesGroup](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
