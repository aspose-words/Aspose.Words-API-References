---
title: "Aspose::Words::Drawing::ReflectionFormat فئة"
linktitle: "ReflectionFormat"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Drawing::ReflectionFormat فئة. يمثل تنسيق الانعكاس لكائن في C++."
type: docs
weight: 9500
url: /ar/cpp/aspose.words.drawing/reflectionformat/
---
## ReflectionFormat class


يمثل تنسيق الانعكاس لكائن.

```cpp
class ReflectionFormat : public System::Object
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [get_Blur](./get_blur/)() | يحصل أو يعيّن قيمة مزدوجة تحدد درجة تأثير الضبابية المطبقة على تأثير الانعكاس بالنقاط. القيمة الافتراضية هي 0.0. |
| [get_Distance](./get_distance/)() | يحصل أو يعيّن قيمة مزدوجة تحدد مقدار الفصل بين الصورة المنعكسة والكائن بالنقاط. القيمة الافتراضية هي 0.0. |
| [get_Size](./get_size/)() | يحصل أو يعيّن قيمة مزدوجة بين 0.0 و 1.0 تمثل حجم الانعكاس كنسبة مئوية من الكائن المنعكس. القيمة الافتراضية هي 0.0. |
| [get_Transparency](./get_transparency/)() | يحصل أو يعيّن قيمة مزدوجة بين 0.0 (معتم) و 1.0 (شفاف) تمثل درجة الشفافية لتأثير الانعكاس. القيمة الافتراضية هي 0.0. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)() | يزيل [ReflectionFormat](./) من الكائن الأب. |
| [set_Blur](./set_blur/)(double) | محدد لـ [Aspose::Words::Drawing::ReflectionFormat::get_Blur](./get_blur/). |
| [set_Distance](./set_distance/)(double) | محدد لـ [Aspose::Words::Drawing::ReflectionFormat::get_Distance](./get_distance/). |
| [set_Size](./set_size/)(double) | محدد لـ [Aspose::Words::Drawing::ReflectionFormat::get_Size](./get_size/). |
| [set_Transparency](./set_transparency/)(double) | محدد لـ [Aspose::Words::Drawing::ReflectionFormat::get_Transparency](./get_transparency/). |
| static [Type](./type/)() |  |
## ملاحظات


استخدم الخاصية [Reflection](../shapebase/get_reflection/) للوصول إلى خصائص الانعكاس لكائن. لا تقوم بإنشاء مثيلات من الفئة [ReflectionFormat](./) مباشرةً.

## أمثلة



يظهر كيفية التفاعل مع تأثير شكل الانعكاس.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Various shapes.docx");
auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));

shape->get_Reflection()->set_Transparency(0.37);
shape->get_Reflection()->set_Size(0.48);
shape->get_Reflection()->set_Blur(17.5);
shape->get_Reflection()->set_Distance(9.2);

doc->Save(get_ArtifactsDir() + u"Shape.Reflection.docx");

doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"Shape.Reflection.docx");
shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));

System::SharedPtr<Aspose::Words::Drawing::ReflectionFormat> reflectionFormat = shape->get_Reflection();

ASSERT_NEAR(0.37, reflectionFormat->get_Transparency(), 0.01);
ASSERT_NEAR(0.48, reflectionFormat->get_Size(), 0.01);
ASSERT_NEAR(17.5, reflectionFormat->get_Blur(), 0.01);
ASSERT_NEAR(9.2, reflectionFormat->get_Distance(), 0.01);

reflectionFormat->Remove();

ASPOSE_ASSERT_EQ(0, reflectionFormat->get_Transparency());
ASPOSE_ASSERT_EQ(0, reflectionFormat->get_Size());
ASPOSE_ASSERT_EQ(0, reflectionFormat->get_Blur());
ASPOSE_ASSERT_EQ(0, reflectionFormat->get_Distance());
```

## انظر أيضًا

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
