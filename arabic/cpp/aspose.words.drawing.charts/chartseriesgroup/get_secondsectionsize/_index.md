---
title: "Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_SecondSectionSize طريقة"
linktitle: "get_SecondSectionSize"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_SecondSectionSize طريقة. يحصل أو يضبط حجم القسم الثانوي لمخطط الفطيرة كنسبة مئوية في C++."
type: docs
weight: 10000
url: /ar/cpp/aspose.words.drawing.charts/chartseriesgroup/get_secondsectionsize/
---
## ChartSeriesGroup::get_SecondSectionSize method


يحصل أو يضبط حجم القسم الثانوي لمخطط الفطيرة كنسبة مئوية.

```cpp
int32_t Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_SecondSectionSize()
```

## ملاحظات


ينطبق على مجموعات السلاسل من نوعي [PieOfPie](../../chartseriestype/) و [PieOfBar](../../chartseriestype/).

نطاق القيم المقبولة هو من 5 إلى 200 شاملًا. القيمة الافتراضية هي 75.

## أمثلة



يظهر كيفية إنشاء وتنسيق مخطط فطيرة داخل فطيرة.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::PieOfPie, 440, 300);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();
// احذف السلسلة التي تم إنشاؤها افتراضيًا.
chart->get_Series()->Clear();

auto categories = System::MakeArray<System::String>({u"Category 1", u"Category 2", u"Category 3", u"Category 4"});
chart->get_Series()->Add(u"Series 1", categories, System::MakeArray<double>({11, 8, 4, 3}));

// قم بتنسيق مخطط فطيرة داخل فطيرة.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeriesGroup> seriesGroup = chart->get_SeriesGroups()->idx_get(0);
seriesGroup->set_GapWidth(10);
seriesGroup->set_SecondSectionSize(77);

doc->Save(get_ArtifactsDir() + u"Charts.PieOfPieChart.docx");
```

## انظر أيضًا

* Class [ChartSeriesGroup](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
