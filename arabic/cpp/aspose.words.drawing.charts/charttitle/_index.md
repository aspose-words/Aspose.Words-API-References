---
title: "Aspose::Words::Drawing::Charts::ChartTitle فئة"
linktitle: "ChartTitle"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Drawing::Charts::ChartTitle فئة. يوفر الوصول إلى خصائص عنوان المخطط. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 18000
url: /ar/cpp/aspose.words.drawing.charts/charttitle/
---
## ChartTitle class


يوفر الوصول إلى خصائص عنوان المخطط. لمعرفة المزيد، قم بزيارة مقالة الوثائق [Working with Charts](https://docs.aspose.com/words/cpp/working-with-charts/).

```cpp
class ChartTitle : public System::Object
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [get_Font](./get_font/)() | يوفر الوصول إلى تنسيق الخط لعنوان المخطط. |
| [get_Format](./get_format/)() | يوفر الوصول إلى تنسيق التعبئة والخط لعنوان المخطط. |
| [get_Orientation](./get_orientation/)() | يحصل أو يضبط اتجاه نص عنوان المخطط. |
| [get_Overlay](./get_overlay/)() | يحدد ما إذا كان يُسمح لعناصر المخطط الأخرى بتغطية العنوان. بشكل افتراضي، التراكب هو **false**. |
| [get_Rotation](./get_rotation/)() | يحصل أو يضبط دوران عنوان المخطط بالدرجات. |
| [get_Show](./get_show/)() | يحدد ما إذا كان يجب إظهار العنوان لهذا المخطط. القيمة الافتراضية هي **true**. |
| [get_Text](./get_text/)() | يحصل أو يضبط نص عنوان المخطط. إذا تم تحديد **null** أو قيمة فارغة، سيتم عرض عنوان مُولد تلقائيًا. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Orientation](./set_orientation/)(Aspose::Words::Drawing::ShapeTextOrientation) | مُعيّن لـ [Aspose::Words::Drawing::Charts::ChartTitle::get_Orientation](./get_orientation/). |
| [set_Overlay](./set_overlay/)(bool) | دالة تعيين لـ [Aspose::Words::Drawing::Charts::ChartTitle::get_Overlay](./get_overlay/). |
| [set_Rotation](./set_rotation/)(int32_t) | دالة تعيين لـ [Aspose::Words::Drawing::Charts::ChartTitle::get_Rotation](./get_rotation/). |
| [set_Show](./set_show/)(bool) | دالة تعيين لـ [Aspose::Words::Drawing::Charts::ChartTitle::get_Show](./get_show/). |
| [set_Text](./set_text/)(const System::String\&) | دالة تعيين لـ [Aspose::Words::Drawing::Charts::ChartTitle::get_Text](./get_text/). |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
