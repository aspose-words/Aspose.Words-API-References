---
title: "طريقة Aspose::Words::Drawing::Charts::ChartSeries::get_Format"
linktitle: "get_Format"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Drawing::Charts::ChartSeries::get_Format. توفر الوصول إلى تنسيق التعبئة والخط للسلسلة في C++."
type: docs
weight: 6000
url: /ar/cpp/aspose.words.drawing.charts/chartseries/get_format/
---
## ChartSeries::get_Format method


يوفر الوصول إلى تنسيق التعبئة والخط للسلسلة.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartFormat> Aspose::Words::Drawing::Charts::ChartSeries::get_Format()
```


## أمثلة



يعرض كيفية تعيين لون السلسلة.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 432, 252);

System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeriesCollection> seriesColl = chart->get_Series();

// حذف السلسلة التي تم إنشاؤها افتراضيًا.
seriesColl->Clear();

// إنشاء مصفوفة أسماء الفئات.
auto categories = System::MakeArray<System::String>({u"Category 1", u"Category 2"});

// إضافة سلسلة جديدة. يجب أن تكون مصفوفات القيم والفئات بنفس الحجم.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series1 = seriesColl->Add(u"Series 1", categories, System::MakeArray<double>({1, 2}));
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series2 = seriesColl->Add(u"Series 2", categories, System::MakeArray<double>({3, 4}));
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series3 = seriesColl->Add(u"Series 3", categories, System::MakeArray<double>({5, 6}));

// تعيين لون السلسلة.
series1->get_Format()->get_Fill()->set_ForeColor(System::Drawing::Color::get_Red());
series2->get_Format()->get_Fill()->set_ForeColor(System::Drawing::Color::get_Yellow());
series3->get_Format()->get_Fill()->set_ForeColor(System::Drawing::Color::get_Blue());

doc->Save(get_ArtifactsDir() + u"Charts.SeriesColor.docx");
```

## انظر أيضًا

* Class [ChartFormat](../../chartformat/)
* Class [ChartSeries](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
