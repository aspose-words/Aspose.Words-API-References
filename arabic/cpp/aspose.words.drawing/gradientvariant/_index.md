---
title: "Aspose::Words::Drawing::GradientVariant enum"
linktitle: "GradientVariant"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Drawing::GradientVariant enum. يحدد المتغير لتعبئة التدرج في C++."
type: docs
weight: 25000
url: /ar/cpp/aspose.words.drawing/gradientvariant/
---
## GradientVariant enum


يحدد المتغير لتعبئة التدرج.

```cpp
enum class GradientVariant
```

### القيم

| الاسم | القيمة | الوصف |
| --- | --- | --- |
| None | 0 | متغير التدرج 'None'. |
| Variant1 | 1 | متغير التدرج 1. |
| Variant2 | 2 | متغير التدرج 2. |
| Variant3 | 3 | متغير التدرج 3. |
| Variant4 | 4 | متغير التدرج 4. |


## أمثلة



يظهر كيفية تعبئة شكل بالتدرجات.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 80, 80);
// تطبيق تعبئة تدرج بلون واحد على الشكل باستخدام ForeColor لتعبئة التدرج.
shape->get_Fill()->OneColorGradient(System::Drawing::Color::get_Red(), Aspose::Words::Drawing::GradientStyle::Horizontal, Aspose::Words::Drawing::GradientVariant::Variant2, 0.1);

ASSERT_EQ(System::Drawing::Color::get_Red().ToArgb(), shape->get_Fill()->get_ForeColor().ToArgb());
ASSERT_EQ(Aspose::Words::Drawing::GradientStyle::Horizontal, shape->get_Fill()->get_GradientStyle());
ASSERT_EQ(Aspose::Words::Drawing::GradientVariant::Variant2, shape->get_Fill()->get_GradientVariant());
ASPOSE_ASSERT_EQ(270, shape->get_Fill()->get_GradientAngle());

shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 80, 80);
// تطبيق تعبئة تدرج بلونين على الشكل.
shape->get_Fill()->TwoColorGradient(Aspose::Words::Drawing::GradientStyle::FromCorner, Aspose::Words::Drawing::GradientVariant::Variant4);
// تغيير BackColor لتعبئة التدرج.
shape->get_Fill()->set_BackColor(System::Drawing::Color::get_Yellow());
// لاحظ أن التغييرات "GradientAngle" لـ "GradientStyle.FromCorner/GradientStyle.FromCenter"
// تعبئة التدرج لا تُحدث أي تأثير، وستعمل فقط مع التدرج الخطي.
shape->get_Fill()->set_GradientAngle(15);

ASSERT_EQ(System::Drawing::Color::get_Yellow().ToArgb(), shape->get_Fill()->get_BackColor().ToArgb());
ASSERT_EQ(Aspose::Words::Drawing::GradientStyle::FromCorner, shape->get_Fill()->get_GradientStyle());
ASSERT_EQ(Aspose::Words::Drawing::GradientVariant::Variant4, shape->get_Fill()->get_GradientVariant());
ASPOSE_ASSERT_EQ(0, shape->get_Fill()->get_GradientAngle());

// استخدم خيار الامتثال لتعريف الشكل باستخدام DML إذا كنت ترغب في الحصول على "GradientStyle",
// "GradientVariant" و "GradientAngle" الخصائص بعد حفظ المستند.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>();
saveOptions->set_Compliance(Aspose::Words::Saving::OoxmlCompliance::Iso29500_2008_Strict);

doc->Save(get_ArtifactsDir() + u"Shape.GradientFill.docx", saveOptions);
```

## انظر أيضًا

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
