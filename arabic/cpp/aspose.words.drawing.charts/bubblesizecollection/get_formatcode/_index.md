---
title: "طريقة Aspose::Words::Drawing::Charts::BubbleSizeCollection::get_FormatCode"
linktitle: "get_FormatCode"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Drawing::Charts::BubbleSizeCollection::get_FormatCode. تحصل أو تعيين رمز التنسيق المطبق على أحجام الفقاعات في C++."
type: docs
weight: 2500
url: /ar/cpp/aspose.words.drawing.charts/bubblesizecollection/get_formatcode/
---
## BubbleSizeCollection::get_FormatCode method


يحصل أو يضبط رمز التنسيق المطبق على أحجام الفقاعات.

```cpp
System::String Aspose::Words::Drawing::Charts::BubbleSizeCollection::get_FormatCode()
```

## ملاحظات


يتم استخدام تنسيق الأرقام لتغيير طريقة ظهور القيم في المخطط. أمثلة على تنسيقات الأرقام:

رقم - "#,##0.00"

عملة - "\"\$\\"#,##0.00"

وقت - "[$-x-systime]h:mm:ss AM/PM"

تاريخ - "d/mm/yyyy"

نسبة مئوية - "0.00%"

كسر - "# ?/?"

علمي - "0.00E+00"

المحاسبة - "_-\"\$\\"* #,##0.00_-;-\"\$\\"* #,##0.00_-;_-\"\$\\"* \"-\\"??_-;_-@_-"

مخصص مع اللون - "[Red]-#,##0.0"

## أمثلة



يوضح كيفية العمل مع رمز التنسيق لبيانات المخطط.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// أدرج مخطط فقاعات.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Bubble, 432, 252);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();

// حذف السلسلة التي تم إنشاؤها افتراضيًا.
chart->get_Series()->Clear();

System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series = chart->get_Series()->Add(u"Series1", System::MakeArray<double>({1, 1.9, 2.45, 3}), System::MakeArray<double>({1, -0.9, 1.82, 0}), System::MakeArray<double>({2, 1.1, 2.95, 2}));

// إظهار تسميات البيانات.
series->set_HasDataLabels(true);
series->get_DataLabels()->set_ShowCategoryName(true);
series->get_DataLabels()->set_ShowValue(true);
series->get_DataLabels()->set_ShowBubbleSize(true);

// حدد رموز تنسيق البيانات.
series->get_XValues()->set_FormatCode(u"#,##0.0#");
series->get_YValues()->set_FormatCode(u"#,##0.0#;[Red]\\-#,##0.0#");
series->get_BubbleSizes()->set_FormatCode(u"#,##0.0#");

doc->Save(get_ArtifactsDir() + u"Charts.FormatCode.docx");
```

## انظر أيضًا

* Class [BubbleSizeCollection](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
