---
title: "Aspose::Words::Drawing::Charts::AxisBuiltInUnit تعداد"
linktitle: "AxisBuiltInUnit"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Drawing::Charts::AxisBuiltInUnit تعداد. يحدد وحدات العرض للمحور في C++."
type: docs
weight: 20000
url: /ar/cpp/aspose.words.drawing.charts/axisbuiltinunit/
---
## AxisBuiltInUnit enum


يحدد وحدات العرض للمحور.

```cpp
enum class AxisBuiltInUnit
```

### القيم

| الاسم | القيمة | الوصف |
| --- | --- | --- |
| None | 0 | يحدد أن القيم على المخطط تُعرض كما هي. |
| مخصص | 1 | يحدد أن القيم على المخطط يجب أن تُقسم على مقسّم يُحدده المستخدم. هذه القيمة غير مدعومة من قبل أنواع المخططات الجديدة في MS Office 2016. |
| مليارات | 2 | يحدد أن القيم على المخطط يجب أن تُقسم على 1,000,000,000. |
| HundredMillions | 3 | يحدد أن القيم على المخطط يجب أن تُقسم على 100,000,000. |
| مئات | 4 | يحدد أن القيم على المخطط يجب أن تُقسم على 100. |
| HundredThousands | 5 | يحدد أن القيم في المخطط يجب أن تُقسم على 100,000. |
| Millions | 6 | يحدد أن القيم في المخطط يجب أن تُقسم على 1,000,000. |
| TenMillions | 7 | يحدد أن القيم في المخطط يجب أن تُقسم على 10,000,000. |
| TenThousands | 8 | يحدد أن القيم في المخطط يجب أن تُقسم على 10,000. |
| Thousands | 9 | يحدد أن القيم في المخطط يجب أن تُقسم على 1,000. |
| Trillions | 10 | يحدد أن القيم في المخطط يجب أن تُقسم على 1,000,000,000,0000. |
| Percentage | 11 | يحدد أن القيم في المخطط يجب أن تُقسم على 0.01. هذه القيمة مدعومة فقط من قبل أنواع المخططات الجديدة في MS Office 2016. |


## أمثلة



يظهر كيفية تعديل علامات الفواصل والقيم المعروضة لمحور المخطط.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Scatter, 450, 250);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();

ASSERT_EQ(1, chart->get_Series()->get_Count());
ASSERT_EQ(u"Y-Values", chart->get_Series()->idx_get(0)->get_Name());

// اضبط علامات الفواصل الصغرى لمحور Y لتشير بعيداً عن منطقة الرسم،
// وعلامات الفواصل الكبرى لتتقاطع مع المحور.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartAxis> axis = chart->get_AxisY();
axis->set_MajorTickMark(Aspose::Words::Drawing::Charts::AxisTickMark::Cross);
axis->set_MinorTickMark(Aspose::Words::Drawing::Charts::AxisTickMark::Outside);

// اضبط محور Y لعرض علامة فاصل كبرى كل 10 وحدات، وعلامة فاصل صغرى كل وحدة واحدة.
axis->set_MajorUnit(10);
axis->set_MinorUnit(1);

// اضبط حدود محور Y إلى -10 و20.
// سيعرض هذا المحور Y الآن 4 علامات فواصل كبرى و27 علامة فاصل صغرى.
axis->get_Scaling()->set_Minimum(System::MakeObject<Aspose::Words::Drawing::Charts::AxisBound>(-10.0));
axis->get_Scaling()->set_Maximum(System::MakeObject<Aspose::Words::Drawing::Charts::AxisBound>(20.0));

// بالنسبة لمحور X، اضبط علامات الفواصل الكبرى كل 10 وحدات،
// وعلامة الفاصل الصغرى كل 2.5 وحدة.
axis = chart->get_AxisX();
axis->set_MajorUnit(10);
axis->set_MinorUnit(2.5);

// قم بتكوين كلا نوعي علامات الفواصل لتظهر داخل منطقة رسم المخطط.
axis->set_MajorTickMark(Aspose::Words::Drawing::Charts::AxisTickMark::Inside);
axis->set_MinorTickMark(Aspose::Words::Drawing::Charts::AxisTickMark::Inside);

// اضبط حدود محور X بحيث يغطي المحور 5 علامات فواصل كبرى و12 علامة فاصل صغرى.
axis->get_Scaling()->set_Minimum(System::MakeObject<Aspose::Words::Drawing::Charts::AxisBound>(-10.0));
axis->get_Scaling()->set_Maximum(System::MakeObject<Aspose::Words::Drawing::Charts::AxisBound>(30.0));
axis->get_TickLabels()->set_Alignment(Aspose::Words::ParagraphAlignment::Right);

ASSERT_EQ(1, axis->get_TickLabels()->get_Spacing());
ASPOSE_ASSERT_EQ(doc, axis->get_DisplayUnit()->get_Document());

// اضبط تسميات العلامات لعرض قيمتها بالملايين.
axis->get_DisplayUnit()->set_Unit(Aspose::Words::Drawing::Charts::AxisBuiltInUnit::Millions);

// يمكننا ضبط قيمة أكثر تحديداً التي ستُظهر بها تسميات العلامات قيمها.
// هذا البيان مكافئ للبيان السابق.
axis->get_DisplayUnit()->set_CustomUnit(1000000);

doc->Save(get_ArtifactsDir() + u"Charts.AxisDisplayUnit.docx");
```

## انظر أيضًا

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
