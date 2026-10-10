---
title: "Aspose::Words::Drawing::Charts::AxisBound فئة"
linktitle: "AxisBound"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Drawing::Charts::AxisBound فئة. تمثّل الحد الأدنى أو الحد الأقصى لقيم المحور. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 1000
url: /ar/cpp/aspose.words.drawing.charts/axisbound/
---
## AxisBound class


يمثل الحد الأدنى أو الأقصى لقيم المحور. لمعرفة المزيد، زر مقالة الوثائق [Working with Charts](https://docs.aspose.com/words/cpp/working-with-charts/).

```cpp
class AxisBound : public System::Object
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [AxisBound](./axisbound/)() | ينشئ مثيلاً جديدًا يشير إلى أن حد المحور يجب أن يُحدَّد تلقائيًا بواسطة تطبيق معالجة النصوص. |
| [AxisBound](./axisbound/)(double) | ينشئ حدًا للمحور ممثلاً كرقم. |
| [AxisBound](./axisbound/)(System::DateTime) | ينشئ حدًا للمحور ممثلاً كقيمة تاريخ/وقت. |
| [Equals](./equals/)(System::SharedPtr\<System::Object\>) override | يحدد ما إذا كان الكائن المحدد مساوٍ في القيمة للكائن الحالي. |
| [get_IsAuto](./get_isauto/)() const | يرجع علامة تشير إلى أن حد المحور يجب أن يُحدَّد تلقائيًا. |
| [get_Value](./get_value/)() const | يرجع القيمة الرقمية لحد المحور. |
| [get_ValueAsDate](./get_valueasdate/)() | يرجع قيمة حد المحور ممثلة كقيمة تاريخ/وقت. |
| [GetHashCode](./gethashcode/)() const override | يعمل كدالة تجزئة لهذا النوع. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [ToString](./tostring/)() const override | يعيد سلسلة سهلة القراءة تعرض قيمة هذا الكائن. |
| static [Type](./type/)() |  |
## ملاحظات


يمكن تحديد الحد كقيمة رقمية أو تاريخ/وقت أو قيمة خاصة "auto".

كائنات هذه الفئة غير قابلة للتغيير.

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

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
