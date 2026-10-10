---
title: "Aspose::Words::Drawing::Charts::ChartNumberFormat class"
linktitle: "ChartNumberFormat"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Drawing::Charts::ChartNumberFormat class. يمثل تنسيق الأرقام للعنصر الأصل. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 15000
url: /ar/cpp/aspose.words.drawing.charts/chartnumberformat/
---
## ChartNumberFormat class


يمثل تنسيق الأرقام للعنصر الأصلي. لمعرفة المزيد، قم بزيارة مقالة الوثائق [Working with Charts](https://docs.aspose.com/words/cpp/working-with-charts/).

```cpp
class ChartNumberFormat : public System::Object
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [get_FormatCode](./get_formatcode/)() | يحصل أو يضبط رمز التنسيق المطبق على تسمية البيانات. |
| [get_IsLinkedToSource](./get_islinkedtosource/)() | يحدد ما إذا كان رمز التنسيق مرتبطًا بخلية المصدر. القيمة الافتراضية هي true. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_FormatCode](./set_formatcode/)(const System::String\&) | محدد لـ [Aspose::Words::Drawing::Charts::ChartNumberFormat::get_FormatCode](./get_formatcode/). |
| [set_IsLinkedToSource](./set_islinkedtosource/)(bool) | محدد لـ [Aspose::Words::Drawing::Charts::ChartNumberFormat::get_IsLinkedToSource](./get_islinkedtosource/). |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
