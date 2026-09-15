---
title: "Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_AxisY طريقة"
linktitle: "get_AxisY"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_AxisY طريقة. يوفّر الوصول إلى خصائص المحور Y لهذه مجموعة السلاسل في C++."
type: docs
weight: 4000
url: /ar/cpp/aspose.words.drawing.charts/chartseriesgroup/get_axisy/
---
## ChartSeriesGroup::get_AxisY method


يوفر الوصول إلى خصائص المحور Y لمجموعة السلاسل هذه.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartAxis> Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_AxisY()
```


## أمثلة



يوضح كيفية العمل مع المحور الثانوي للرسم البياني.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Line, 450, 250);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeriesCollection> series = chart->get_Series();

// حذف السلسلة التي تم إنشاؤها افتراضيًا.
series->Clear();

auto categories = System::MakeArray<System::String>({u"Category 1", u"Category 2", u"Category 3"});
series->Add(u"Series 1 of primary series group", categories, System::MakeArray<double>({2, 3, 4}));
series->Add(u"Series 2 of primary series group", categories, System::MakeArray<double>({5, 2, 3}));

// أنشئ مجموعة سلسلة إضافية، أيضًا من نوع الخط.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeriesGroup> newSeriesGroup = chart->get_SeriesGroups()->Add(Aspose::Words::Drawing::Charts::ChartSeriesType::Line);
// حدد استخدام المحاور الثانوية لمجموعة السلسلة الجديدة.
newSeriesGroup->set_AxisGroup(Aspose::Words::Drawing::Charts::AxisGroup::Secondary);
// إخفاء المحور X الثانوي.
newSeriesGroup->get_AxisX()->set_Hidden(true);
// حدد عنوان المحور Y الثانوي.
newSeriesGroup->get_AxisY()->get_Title()->set_Show(true);
newSeriesGroup->get_AxisY()->get_Title()->set_Text(u"Secondary Y axis");

ASSERT_EQ(Aspose::Words::Drawing::Charts::ChartSeriesType::Line, newSeriesGroup->get_SeriesType());

// أضف سلسلة إلى مجموعة السلسلة الجديدة.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series3 = newSeriesGroup->get_Series()->Add(u"Series of secondary series group", categories, System::MakeArray<double>({13, 11, 16}));
series3->get_Format()->get_Stroke()->set_Weight(3.5);

doc->Save(get_ArtifactsDir() + u"Charts.SecondaryAxis.docx");
```

## انظر أيضًا

* Class [ChartAxis](../../chartaxis/)
* Class [ChartSeriesGroup](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
