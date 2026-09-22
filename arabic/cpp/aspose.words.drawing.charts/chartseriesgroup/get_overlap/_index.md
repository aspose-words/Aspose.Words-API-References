---
title: "طريقة Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_Overlap. يحصل على أو يضبط النسبة المئوية لمدى تداخل أشرطة أو أعمدة السلسلة في C++."
linktitle: "ينطبق على مجموعات السلاسل لجميع أنواع الأشرطة والأعمدة."
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_Overlap طريقة. يحصل أو يضبط النسبة المئوية لمقدار تداخل أعمدة أو أشرطة السلسلة في C++."
type: docs
weight: 9000
url: /ar/cpp/aspose.words.drawing.charts/chartseriesgroup/get_overlap/
---
## ChartSeriesGroup::get_Overlap method


يحصل أو يضبط النسبة المئوية لمقدار تداخل أشرطة أو أعمدة السلسلة.

```cpp
int32_t Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_Overlap()
```

## ملاحظات


ينطبق على مجموعات السلسلة لجميع أنواع الأعمدة والأشرطة.

النطاق المقبول للقيم هو من -100 إلى 100 شاملًا. قيمة 0 تشير إلى عدم وجود مساحة بين الأعمدة/الأشرطة. إذا كانت القيمة -100، فإن المسافة بين الأعمدة/الأشرطة تساوي عرضها. قيمة 100 تعني أن الأعمدة/الأشرطة تتداخل تمامًا.

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
