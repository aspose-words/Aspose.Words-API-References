---
title: "طريقة Aspose::Words::Drawing::Charts::ChartAxis::get_Hidden"
linktitle: "get_Hidden"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Drawing::Charts::ChartAxis::get_Hidden. تحصل أو تعيّن علامة تشير إلى ما إذا كان هذا المحور مخفيًا أم لا في C++."
type: docs
weight: 11000
url: /ar/cpp/aspose.words.drawing.charts/chartaxis/get_hidden/
---
## ChartAxis::get_Hidden method


يحصل أو يعيّن علمًا يشير إلى ما إذا كان هذا المحور مخفيًا أم لا.

```cpp
bool Aspose::Words::Drawing::Charts::ChartAxis::get_Hidden()
```


## أمثلة



يوضح كيفية إخفاء محاور المخطط.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Line, 500, 300);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();

// امسح سلسلة بيانات العرض التجريبية للمخطط للبدء بمخطط نظيف.
chart->get_Series()->Clear();

// أضف سلسلة مخصصة مع فئات للمحور X، والقيم العشرية المقابلة للمحور Y.
chart->get_Series()->Add(u"AW Series 1", System::MakeArray<System::String>({u"Item 1", u"Item 2", u"Item 3", u"Item 4", u"Item 5"}), System::MakeArray<double>({1.2, 0.3, 2.1, 2.9, 4.2}));

// إخفاء محاور المخطط لتبسيط مظهر المخطط.
chart->get_AxisX()->set_Hidden(true);
chart->get_AxisY()->set_Hidden(true);

doc->Save(get_ArtifactsDir() + u"Charts.HideChartAxis.docx");
```

## انظر أيضًا

* Class [ChartAxis](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
