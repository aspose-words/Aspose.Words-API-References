---
title: "Aspose::Words::Drawing::Charts::ChartTitle::get_Overlay طريقة"
linktitle: "get_Overlay"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Drawing::Charts::ChartTitle::get_Overlay طريقة. تحدد ما إذا كان يُسمح لعناصر المخطط الأخرى بتغطية العنوان. بشكل افتراضي overlay هو false في C++."
type: docs
weight: 2000
url: /ar/cpp/aspose.words.drawing.charts/charttitle/get_overlay/
---
## ChartTitle::get_Overlay method


يحدد ما إذا كان يُسمح لعناصر المخطط الأخرى بتغطية العنوان. بشكل افتراضي، التراكب هو **false**.

```cpp
bool Aspose::Words::Drawing::Charts::ChartTitle::get_Overlay()
```


## أمثلة



يظهر كيفية إدراج مخطط وتعيين عنوان.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// أدرج شكل مخطط باستخدام منشئ المستند واحصل على مخططه.
System::SharedPtr<Aspose::Words::Drawing::Shape> chartShape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Bar, 400, 300);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = chartShape->get_Chart();

// استخدم خاصية "Title" لإعطاء مخططنا عنوانًا، يظهر في أعلى وسط منطقة المخطط.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartTitle> title = chart->get_Title();
title->set_Text(u"My Chart");
title->get_Font()->set_Size(15);
title->get_Font()->set_Color(System::Drawing::Color::get_Blue());

// اضبط خاصية "Show" إلى "true" لجعل العنوان مرئيًا.
title->set_Show(true);

// اضبط خاصية "Overlay" إلى "true" لمنح عناصر المخطط الأخرى مساحة أكبر بالسماح لها بتغطية العنوان.
title->set_Overlay(true);

doc->Save(get_ArtifactsDir() + u"Charts.ChartTitle.docx");
```

## انظر أيضًا

* Class [ChartTitle](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
