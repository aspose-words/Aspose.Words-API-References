---
title: "طريقة Aspose::Words::Drawing::Charts::Chart::get_Title"
linktitle: "get_Title"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Drawing::Charts::Chart::get_Title. توفر إمكانية الوصول إلى خصائص عنوان المخطط في C++."
type: docs
weight: 8000
url: /ar/cpp/aspose.words.drawing.charts/chart/get_title/
---
## Chart::get_Title method


يوفر الوصول إلى خصائص عنوان المخطط.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartTitle> Aspose::Words::Drawing::Charts::Chart::get_Title()
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

* Class [ChartTitle](../../charttitle/)
* Class [Chart](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
