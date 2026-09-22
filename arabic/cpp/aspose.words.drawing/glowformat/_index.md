---
title: "فئة Aspose::Words::Drawing::GlowFormat"
linktitle: "GlowFormat"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "فئة Aspose::Words::Drawing::GlowFormat. تمثل تنسيق التوهج لكائن في C++."
type: docs
weight: 1500
url: /ar/cpp/aspose.words.drawing/glowformat/
---
## GlowFormat class


يمثل تنسيق التوهج لكائن.

```cpp
class GlowFormat : public System::Object
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [get_Color](./get_color/)() | يسترجع أو يعيّن كائن **Color** الذي يمثل اللون لتأثير التوهج. القيمة الافتراضية هي **Black**. |
| [get_Radius](./get_radius/)() | يسترجع أو يعيّن قيمة مزدوجة تمثل طول نصف القطر لتأثير التوهج بالنقاط (pt). القيمة الافتراضية هي 0.0. |
| [get_Transparency](./get_transparency/)() | يسترجع أو يعيّن درجة الشفافية لتأثير التوهج كقيمة بين 0.0 (معتم) و 1.0 (شفاف). القيمة الافتراضية هي 0.0. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)() | يزيل [GlowFormat](./) من الكائن الأب. |
| [set_Color](./set_color/)(System::Drawing::Color) | مُعيّن لـ [Aspose::Words::Drawing::GlowFormat::get_Color](./get_color/). |
| [set_Radius](./set_radius/)(double) | مُعيّن لـ [Aspose::Words::Drawing::GlowFormat::get_Radius](./get_radius/). |
| [set_Transparency](./set_transparency/)(double) | مُعيّن لـ [Aspose::Words::Drawing::GlowFormat::get_Transparency](./get_transparency/). |
| static [Type](./type/)() |  |
## ملاحظات


استخدم الخاصية [Glow](../shapebase/get_glow/) للوصول إلى خصائص التوهج لكائن. لا تقوم بإنشاء مثيلات من الفئة [GlowFormat](./) مباشرة.

## أمثلة



يظهر كيفية التفاعل مع تأثير شكل التوهج.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Various shapes.docx");
auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));

shape->get_Glow()->set_Color(System::Drawing::Color::get_Salmon());
shape->get_Glow()->set_Radius(30);
shape->get_Glow()->set_Transparency(0.15);

doc->Save(get_ArtifactsDir() + u"Shape.Glow.docx");

doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"Shape.Glow.docx");
shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));

ASSERT_EQ(System::Drawing::Color::FromArgb(217, 250, 128, 114).ToArgb(), shape->get_Glow()->get_Color().ToArgb());
ASPOSE_ASSERT_EQ(30, shape->get_Glow()->get_Radius());
ASSERT_NEAR(0.15, shape->get_Glow()->get_Transparency(), 0.01);

shape->get_Glow()->Remove();

ASSERT_EQ(System::Drawing::Color::get_Black().ToArgb(), shape->get_Glow()->get_Color().ToArgb());
ASPOSE_ASSERT_EQ(0, shape->get_Glow()->get_Radius());
ASPOSE_ASSERT_EQ(0, shape->get_Glow()->get_Transparency());
```

## انظر أيضًا

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
