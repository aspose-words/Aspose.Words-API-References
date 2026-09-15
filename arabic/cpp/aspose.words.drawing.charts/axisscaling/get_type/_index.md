---
title: "طريقة Aspose::Words::Drawing::Charts::AxisScaling::get_Type"
linktitle: "get_Type"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Drawing::Charts::AxisScaling::get_Type. يحصل أو يضبط نوع التحجيم للمحور في C++."
type: docs
weight: 6000
url: /ar/cpp/aspose.words.drawing.charts/axisscaling/get_type/
---
## AxisScaling::get_Type method


يحصل أو يعيّن نوع التحجيم للمحور.

```cpp
Aspose::Words::Drawing::Charts::AxisScaleType Aspose::Words::Drawing::Charts::AxisScaling::get_Type() const
```


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

* Enum [AxisScaleType](../../axisscaletype/)
* Class [AxisScaling](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
