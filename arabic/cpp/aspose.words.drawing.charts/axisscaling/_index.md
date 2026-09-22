---
title: "فئة Aspose::Words::Drawing::Charts::AxisScaling"
linktitle: "AxisScaling"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "فئة Aspose::Words::Drawing::Charts::AxisScaling. تمثل خيارات التحجيم للمحور. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 3000
url: /ar/cpp/aspose.words.drawing.charts/axisscaling/
---
## AxisScaling class


يمثل خيارات التحجيم للمحور. لمعرفة المزيد، زر مقالة الوثائق [Working with Charts](https://docs.aspose.com/words/cpp/working-with-charts/).

```cpp
class AxisScaling : public Aspose::Words::Drawing::Core::Dml::IDmlExtensionListSource
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [AxisScaling](./axisscaling/)() |  |
| [get_LogBase](./get_logbase/)() const | يحصل أو يعيّن القاعدة اللوغاريتمية للمحور اللوغاريتمي. |
| [get_Maximum](./get_maximum/)() | يحصل أو يعيّن القيمة القصوى للمحور. |
| [get_Minimum](./get_minimum/)() | يحصل أو يعيّن القيمة الدنيا للمحور. |
| [get_Type](./get_type/)() const | يحصل أو يعيّن نوع التحجيم للمحور. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_LogBase](./set_logbase/)(double) | دالة تعيين لـ [Aspose::Words::Drawing::Charts::AxisScaling::get_LogBase](./get_logbase/). |
| [set_Maximum](./set_maximum/)(const System::SharedPtr\<Aspose::Words::Drawing::Charts::AxisBound\>\&) | دالة تعيين لـ [Aspose::Words::Drawing::Charts::AxisScaling::get_Maximum](./get_maximum/). |
| [set_Minimum](./set_minimum/)(const System::SharedPtr\<Aspose::Words::Drawing::Charts::AxisBound\>\&) | دالة تعيين لـ [Aspose::Words::Drawing::Charts::AxisScaling::get_Minimum](./get_minimum/). |
| [set_Type](./set_type/)(Aspose::Words::Drawing::Charts::AxisScaleType) | دالة تعيين لـ [Aspose::Words::Drawing::Charts::AxisScaling::get_Type](./get_type/). |
| static [Type](./type/)() |  |

## أمثلة



يعرض كيفية تطبيق التحجيم اللوغاريتمي على محور المخطط.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> chartShape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Scatter, 450, 300);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = chartShape->get_Chart();

// امسح سلسلة بيانات العرض التجريبية للمخطط للبدء بمخطط نظيف.
chart->get_Series()->Clear();

// أدرج سلسلة بإحداثيات X/Y لخمسة نقاط.
chart->get_Series()->Add(u"Series 1", System::MakeArray<double>({1.0, 2.0, 3.0, 4.0, 5.0}), System::MakeArray<double>({1.0, 20.0, 400.0, 8000.0, 160000.0}));

// التحجيم لمحور X هو خطّي بشكل افتراضي،
// معرضًا قيمًا تتزايد بالتساوي تغطي نطاق قيم X لدينا (0، 1، 2، 3...).
// محور خطّي ليس مثالياً لقيم Y لدينا
// لأن النقاط ذات قيم Y الأصغر ستكون أصعب في القراءة.
// تحجيم لوغاريتمي بقاعدة 20 (1، 20، 400، 8000...)
// سيفرق النقاط المرسومة، مما يسمح لنا بقراءة قيمها على المخطط بسهولة أكبر.
chart->get_AxisY()->get_Scaling()->set_Type(Aspose::Words::Drawing::Charts::AxisScaleType::Logarithmic);
chart->get_AxisY()->get_Scaling()->set_LogBase(20);

doc->Save(get_ArtifactsDir() + u"Charts.AxisScaling.docx");
```

## انظر أيضًا

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
