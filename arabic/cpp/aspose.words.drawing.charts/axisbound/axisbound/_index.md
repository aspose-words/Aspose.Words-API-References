---
title: "منشئ Aspose::Words::Drawing::Charts::AxisBound::AxisBound"
linktitle: "AxisBound"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "منشئ Aspose::Words::Drawing::Charts::AxisBound::AxisBound. ينشئ نسخة جديدة تشير إلى أن حد المحور يجب أن يُحدد تلقائيًا بواسطة تطبيق معالجة النصوص في C++."
type: docs
weight: 2000
url: /ar/cpp/aspose.words.drawing.charts/axisbound/axisbound/
---
## AxisBound::AxisBound() constructor


ينشئ مثيلاً جديدًا يشير إلى أن حد المحور يجب أن يُحدَّد تلقائيًا بواسطة تطبيق معالجة النصوص.

```cpp
Aspose::Words::Drawing::Charts::AxisBound::AxisBound()
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
## AxisBound::AxisBound(double) constructor


ينشئ حدًا للمحور ممثلاً كرقم.

```cpp
Aspose::Words::Drawing::Charts::AxisBound::AxisBound(double value)
```


## أمثلة



يظهر كيفية إدراج مخطط بقيم تاريخ/وقت.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Line, 500, 300);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();

// امسح سلسلة بيانات العرض التجريبية للمخطط للبدء بمخطط نظيف.
chart->get_Series()->Clear();

// أضف سلسلة مخصصة تحتوي على قيم تاريخ/وقت للمحور X، وقيم عشرية مقابلة للمحور Y.
chart->get_Series()->Add(u"Aspose Test Series", System::MakeArray<System::DateTime>({System::DateTime(2017, 11, 6), System::DateTime(2017, 11, 9), System::DateTime(2017, 11, 15), System::DateTime(2017, 11, 21), System::DateTime(2017, 11, 25), System::DateTime(2017, 11, 29)}), System::MakeArray<double>({1.2, 0.3, 2.1, 2.9, 4.2, 5.3}));

// حدد الحدود السفلية والعلوية للمحور X.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartAxis> xAxis = chart->get_AxisX();
xAxis->get_Scaling()->set_Minimum(System::MakeObject<Aspose::Words::Drawing::Charts::AxisBound>(System::DateTime(2017, 11, 5).ToOADate()));
xAxis->get_Scaling()->set_Maximum(System::MakeObject<Aspose::Words::Drawing::Charts::AxisBound>(System::DateTime(2017, 12, 3)));

// حدد الوحدات الرئيسية للمحور X إلى أسبوع، والوحدات الثانوية إلى يوم.
xAxis->set_BaseTimeUnit(Aspose::Words::Drawing::Charts::AxisTimeUnit::Days);
xAxis->set_MajorUnit(7.0);
xAxis->set_MajorTickMark(Aspose::Words::Drawing::Charts::AxisTickMark::Cross);
xAxis->set_MinorUnit(1.0);
xAxis->set_MinorTickMark(Aspose::Words::Drawing::Charts::AxisTickMark::Outside);
xAxis->set_HasMajorGridlines(true);
xAxis->set_HasMinorGridlines(true);

// عرّف خصائص المحور Y للقيم العشرية.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartAxis> yAxis = chart->get_AxisY();
yAxis->get_TickLabels()->set_Position(Aspose::Words::Drawing::Charts::AxisTickLabelPosition::High);
yAxis->set_MajorUnit(100.0);
yAxis->set_MinorUnit(50.0);
yAxis->get_DisplayUnit()->set_Unit(Aspose::Words::Drawing::Charts::AxisBuiltInUnit::Hundreds);
yAxis->get_Scaling()->set_Minimum(System::MakeObject<Aspose::Words::Drawing::Charts::AxisBound>(100.0));
yAxis->get_Scaling()->set_Maximum(System::MakeObject<Aspose::Words::Drawing::Charts::AxisBound>(700.0));
yAxis->set_HasMajorGridlines(true);
yAxis->set_HasMinorGridlines(true);

doc->Save(get_ArtifactsDir() + u"Charts.DateTimeValues.docx");
```

## انظر أيضًا

* Class [AxisBound](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
## AxisBound::AxisBound(System::DateTime) constructor


ينشئ حدًا للمحور ممثلاً كقيمة تاريخ/وقت.

```cpp
Aspose::Words::Drawing::Charts::AxisBound::AxisBound(System::DateTime datetime)
```


## أمثلة



يظهر كيفية إدراج مخطط بقيم تاريخ/وقت.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Line, 500, 300);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();

// امسح سلسلة بيانات العرض التجريبية للمخطط للبدء بمخطط نظيف.
chart->get_Series()->Clear();

// أضف سلسلة مخصصة تحتوي على قيم تاريخ/وقت للمحور X، وقيم عشرية مقابلة للمحور Y.
chart->get_Series()->Add(u"Aspose Test Series", System::MakeArray<System::DateTime>({System::DateTime(2017, 11, 6), System::DateTime(2017, 11, 9), System::DateTime(2017, 11, 15), System::DateTime(2017, 11, 21), System::DateTime(2017, 11, 25), System::DateTime(2017, 11, 29)}), System::MakeArray<double>({1.2, 0.3, 2.1, 2.9, 4.2, 5.3}));

// حدد الحدود السفلية والعلوية للمحور X.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartAxis> xAxis = chart->get_AxisX();
xAxis->get_Scaling()->set_Minimum(System::MakeObject<Aspose::Words::Drawing::Charts::AxisBound>(System::DateTime(2017, 11, 5).ToOADate()));
xAxis->get_Scaling()->set_Maximum(System::MakeObject<Aspose::Words::Drawing::Charts::AxisBound>(System::DateTime(2017, 12, 3)));

// حدد الوحدات الرئيسية للمحور X إلى أسبوع، والوحدات الثانوية إلى يوم.
xAxis->set_BaseTimeUnit(Aspose::Words::Drawing::Charts::AxisTimeUnit::Days);
xAxis->set_MajorUnit(7.0);
xAxis->set_MajorTickMark(Aspose::Words::Drawing::Charts::AxisTickMark::Cross);
xAxis->set_MinorUnit(1.0);
xAxis->set_MinorTickMark(Aspose::Words::Drawing::Charts::AxisTickMark::Outside);
xAxis->set_HasMajorGridlines(true);
xAxis->set_HasMinorGridlines(true);

// عرّف خصائص المحور Y للقيم العشرية.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartAxis> yAxis = chart->get_AxisY();
yAxis->get_TickLabels()->set_Position(Aspose::Words::Drawing::Charts::AxisTickLabelPosition::High);
yAxis->set_MajorUnit(100.0);
yAxis->set_MinorUnit(50.0);
yAxis->get_DisplayUnit()->set_Unit(Aspose::Words::Drawing::Charts::AxisBuiltInUnit::Hundreds);
yAxis->get_Scaling()->set_Minimum(System::MakeObject<Aspose::Words::Drawing::Charts::AxisBound>(100.0));
yAxis->get_Scaling()->set_Maximum(System::MakeObject<Aspose::Words::Drawing::Charts::AxisBound>(700.0));
yAxis->set_HasMajorGridlines(true);
yAxis->set_HasMinorGridlines(true);

doc->Save(get_ArtifactsDir() + u"Charts.DateTimeValues.docx");
```

## انظر أيضًا

* Class [AxisBound](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
