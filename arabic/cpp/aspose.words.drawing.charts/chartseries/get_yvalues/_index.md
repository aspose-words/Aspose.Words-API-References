---
title: "Aspose::Words::Drawing::Charts::ChartSeries::get_YValues طريقة"
linktitle: "get_YValues"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Drawing::Charts::ChartSeries::get_YValues طريقة. يحصل على مجموعة من قيم Y لهذه السلسلة البيانية في C++."
type: docs
weight: 12667
url: /ar/cpp/aspose.words.drawing.charts/chartseries/get_yvalues/
---
## ChartSeries::get_YValues method


يحصل على مجموعة من قيم Y لهذه السلسلة البيانية.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartYValueCollection> Aspose::Words::Drawing::Charts::ChartSeries::get_YValues()
```


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

* Class [ChartYValueCollection](../../chartyvaluecollection/)
* Class [ChartSeries](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
