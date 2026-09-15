---
title: "طريقة Aspose::Words::Drawing::Charts::ChartNumberFormat::get_FormatCode"
linktitle: "get_FormatCode"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Drawing::Charts::ChartNumberFormat::get_FormatCode. يحصل أو يضبط رمز التنسيق المطبق على تسمية البيانات في C++."
type: docs
weight: 2000
url: /ar/cpp/aspose.words.drawing.charts/chartnumberformat/get_formatcode/
---
## ChartNumberFormat::get_FormatCode method


يحصل أو يضبط رمز التنسيق المطبق على تسمية البيانات.

```cpp
System::String Aspose::Words::Drawing::Charts::ChartNumberFormat::get_FormatCode()
```

## ملاحظات


يتم استخدام تنسيق الأرقام لتغيير طريقة ظهور القيمة في تسمية البيانات ويمكن استخدامه بطرق إبداعية جدًا. أمثلة تنسيقات الأرقام:

رقم - "#,##0.00"

عملة - "\"\$\\"#,##0.00"

وقت - "[$-x-systime]h:mm:ss AM/PM"

تاريخ - "d/mm/yyyy"

نسبة مئوية - "0.00%"

كسر - "# ?/?"

علمي - "0.00E+00"

نص - "@"

المحاسبة - "_-\"\$\\"* #,##0.00_-;-\"\$\\"* #,##0.00_-;_-\"\$\\"* \"-\\"??_-;_-@_-"

مخصص مع اللون - "[Red]-#,##0.0"

## أمثلة



يعرض كيفية تمكين وتكوين تسميات البيانات لسلسلة مخطط.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// أضف مخطط خطي، ثم امسح سلسلة البيانات التجريبية الخاصة به للبدء بمخطط نظيف،
// ثم قم بتعيين عنوان.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Line, 500, 300);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();
chart->get_Series()->Clear();
chart->get_Title()->set_Text(u"Monthly sales report");

// أدرج سلسلة مخطط مخصصة مع الأشهر كفئات للمحور X،
// ومبالغ عشرية مقابلة للمحور Y.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series = chart->get_Series()->Add(u"Revenue", System::MakeArray<System::String>({u"January", u"February", u"March"}), System::MakeArray<double>({25.611, 21.439, 33.750}));

// فعّل تسميات البيانات، ثم طبّق تنسيق رقم مخصص للقيم المعروضة في تسميات البيانات.
// سيعامل هذا التنسيق القيم العشرية المعروضة كملّيين من الدولار الأمريكي.
series->set_HasDataLabels(true);
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartDataLabelCollection> dataLabels = series->get_DataLabels();
dataLabels->set_ShowValue(true);
dataLabels->get_NumberFormat()->set_FormatCode(u"\"US$\" #,##0.000\"M\"");
dataLabels->get_Font()->set_Size(12);

doc->Save(get_ArtifactsDir() + u"Charts.DataLabelNumberFormat.docx");
```


يعرض كيفية تعيين تنسيق قيم المخطط.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 500, 300);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();

// امسح سلسلة بيانات العرض التجريبية للمخطط للبدء بمخطط نظيف.
chart->get_Series()->Clear();

// أضف سلسلة مخصصة إلى المخطط مع فئات لمحور X،
// وقيم عددية كبيرة مناسبة لمحور Y.
chart->get_Series()->Add(u"Aspose Test Series", System::MakeArray<System::String>({u"Word", u"PDF", u"Excel", u"GoogleDocs", u"Note"}), System::MakeArray<double>({1900000, 850000, 2100000, 600000, 1500000}));

// عيّن تنسيق الأرقام لتسميات علامات محور Y بحيث لا يتم تجميع الأرقام بفواصل.
chart->get_AxisY()->get_NumberFormat()->set_FormatCode(u"#,##0");

// يمكن لهذه العلامة تجاوز القيمة السابقة واستخراج تنسيق الرقم من خلية المصدر.
ASSERT_FALSE(chart->get_AxisY()->get_NumberFormat()->get_IsLinkedToSource());

doc->Save(get_ArtifactsDir() + u"Charts.SetNumberFormatToChartAxis.docx");
```

## انظر أيضًا

* Class [ChartNumberFormat](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
