---
title: "طريقة Aspose::Words::Drawing::Charts::AxisBound::get_Value"
linktitle: "get_Value"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Drawing::Charts::AxisBound::get_Value. تُرجع القيمة الرقمية للحد المحوري في C++."
type: docs
weight: 5000
url: /ar/cpp/aspose.words.drawing.charts/axisbound/get_value/
---
## AxisBound::get_Value method


يرجع القيمة الرقمية لحد المحور.

```cpp
double Aspose::Words::Drawing::Charts::AxisBound::get_Value() const
```


## أمثلة



يظهر كيفية تعيين حدود محاور مخصصة.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> chartShape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Scatter, 450, 300);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = chartShape->get_Chart();

// امسح سلسلة بيانات العرض التجريبية للمخطط للبدء بمخطط نظيف.
chart->get_Series()->Clear();

// أضف سلسلة تحتوي على مصفوفتين عشريتين. المصفوفة الأولى تحتوي على قيم X،
// والثانية تحتوي على قيم Y المقابلة للنقاط في مخطط التشتت.
chart->get_Series()->Add(u"Series 1", System::MakeArray<double>({1.1, 5.4, 7.9, 3.5, 2.1, 9.7}), System::MakeArray<double>({2.1, 0.3, 0.6, 3.3, 1.4, 1.9}));

// بشكل افتراضي، يتم تطبيق التحجيم الافتراضي على محوري X و Y للرسم البياني،
// بحيث تكون نطاقاتهما كبيرة بما يكفي لتشمل كل قيمة X و Y لكل سلسلة.
ASSERT_TRUE(chart->get_AxisX()->get_Scaling()->get_Minimum()->get_IsAuto());

// يمكننا تعريف حدود محاورنا الخاصة.
// في هذه الحالة، سنجعل كل من محوري X و Y يظهران نطاقًا من 0 إلى 10.
chart->get_AxisX()->get_Scaling()->set_Minimum(System::MakeObject<Aspose::Words::Drawing::Charts::AxisBound>(0.0));
chart->get_AxisX()->get_Scaling()->set_Maximum(System::MakeObject<Aspose::Words::Drawing::Charts::AxisBound>(10.0));
chart->get_AxisY()->get_Scaling()->set_Minimum(System::MakeObject<Aspose::Words::Drawing::Charts::AxisBound>(0.0));
chart->get_AxisY()->get_Scaling()->set_Maximum(System::MakeObject<Aspose::Words::Drawing::Charts::AxisBound>(10.0));

ASSERT_FALSE(chart->get_AxisX()->get_Scaling()->get_Minimum()->get_IsAuto());
ASSERT_FALSE(chart->get_AxisY()->get_Scaling()->get_Minimum()->get_IsAuto());

// أنشئ مخططًا خطيًا بسلسلة تحتاج إلى نطاق من التواريخ على محور X، وقيم عشرية لمحور Y.
chartShape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Line, 450, 300);
chart = chartShape->get_Chart();
chart->get_Series()->Clear();

System::ArrayPtr<System::DateTime> dates = System::MakeArray<System::DateTime>({System::DateTime(1973, 5, 11), System::DateTime(1981, 2, 4), System::DateTime(1985, 9, 23), System::DateTime(1989, 6, 28), System::DateTime(1994, 12, 15)});

chart->get_Series()->Add(u"Series 1", dates, System::MakeArray<double>({3.0, 4.7, 5.9, 7.1, 8.9}));

// يمكننا أيضًا تعيين حدود المحور على شكل تواريخ، لتقييد المخطط بفترة زمنية.
// تعيين النطاق إلى 1980-1990 سيحذف قيمتين من قيم السلسلة
// التي تقع خارج النطاق من الرسم البياني.
chart->get_AxisX()->get_Scaling()->set_Minimum(System::MakeObject<Aspose::Words::Drawing::Charts::AxisBound>(System::DateTime(1980, 1, 1)));
chart->get_AxisX()->get_Scaling()->set_Maximum(System::MakeObject<Aspose::Words::Drawing::Charts::AxisBound>(System::DateTime(1990, 1, 1)));

doc->Save(get_ArtifactsDir() + u"Charts.AxisBound.docx");
```

## انظر أيضًا

* Class [AxisBound](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
