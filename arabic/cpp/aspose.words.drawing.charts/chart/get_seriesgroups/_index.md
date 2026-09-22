---
title: "طريقة Aspose::Words::Drawing::Charts::Chart::get_SeriesGroups"
linktitle: "get_SeriesGroups"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Drawing::Charts::Chart::get_SeriesGroups. توفر إمكانية الوصول إلى مجموعة مجموعات السلاسل لهذا المخطط في C++."
type: docs
weight: 6500
url: /ar/cpp/aspose.words.drawing.charts/chart/get_seriesgroups/
---
## Chart::get_SeriesGroups method


يوفر الوصول إلى مجموعة مجموعات السلاسل لهذا المخطط.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeriesGroupCollection> Aspose::Words::Drawing::Charts::Chart::get_SeriesGroups()
```


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

* Class [ChartSeriesGroupCollection](../../chartseriesgroupcollection/)
* Class [Chart](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
