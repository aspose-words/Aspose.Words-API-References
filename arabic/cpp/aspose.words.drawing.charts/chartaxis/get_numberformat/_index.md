---
title: "طريقة Aspose::Words::Drawing::Charts::ChartAxis::get_NumberFormat"
linktitle: "get_NumberFormat"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Drawing::Charts::ChartAxis::get_NumberFormat. تُرجع كائن ChartNumberFormat يتيح تعريف تنسيقات الأرقام للمحور في C++."
type: docs
weight: 20000
url: /ar/cpp/aspose.words.drawing.charts/chartaxis/get_numberformat/
---
## ChartAxis::get_NumberFormat method


تُرجع كائنًا [ChartNumberFormat](../../chartnumberformat/) يتيح تعريف تنسيقات الأرقام للمحور.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartNumberFormat> Aspose::Words::Drawing::Charts::ChartAxis::get_NumberFormat()
```


## أمثلة



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

* Class [ChartNumberFormat](../../chartnumberformat/)
* Class [ChartAxis](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
