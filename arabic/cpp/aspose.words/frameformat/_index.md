---
title: "الفئة Aspose::Words::FrameFormat"
linktitle: "FrameFormat"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "الفئة Aspose::Words::FrameFormat. تمثل تنسيق الإطار المتعلق بفقرة في C++."
type: docs
weight: 30000
url: /ar/cpp/aspose.words/frameformat/
---
## FrameFormat class


يمثل تنسيقًا متعلقًا بالإطار لفقرة.

```cpp
class FrameFormat : public System::Object
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [get_Height](./get_height/)() | يحصل على ارتفاع الإطار المحدد. |
| [get_HeightRule](./get_heightrule/)() | يحصل على القاعدة لتحديد ارتفاع الإطار المحدد. |
| [get_HorizontalAlignment](./get_horizontalalignment/)() | يحصل على المحاذاة الأفقية للإطار المحدد. |
| [get_HorizontalDistanceFromText](./get_horizontaldistancefromtext/)() | يحصل على المسافة الأفقية بين الإطار والنص المحيط، بالنقاط. |
| [get_HorizontalPosition](./get_horizontalposition/)() | يحصل على المسافة الأفقية بين حافة الإطار والعنصر المحدد بواسطة خاصية [RelativeHorizontalPosition](./get_relativehorizontalposition/). |
| [get_IsFrame](./get_isframe/)() | يرجع **true** إذا كانت الفقرة إطارًا. |
| [get_RelativeHorizontalPosition](./get_relativehorizontalposition/)() | يحصل على الموضع الأفقي النسبي لإطار. |
| [get_RelativeVerticalPosition](./get_relativeverticalposition/)() | يحصل على الموضع الرأسي النسبي لإطار. |
| [get_VerticalAlignment](./get_verticalalignment/)() | يحصل على المحاذاة الرأسية للإطار المحدد. |
| [get_VerticalDistanceFromText](./get_verticaldistancefromtext/)() | يحدد المسافة الرأسية (بالنقاط) بين الإطار والنص المحيط. |
| [get_VerticalPosition](./get_verticalposition/)() | يحصل على المسافة الرأسية بين حافة الإطار والعنصر المحدد بواسطة خاصية [RelativeVerticalPosition](./get_relativeverticalposition/). |
| [get_Width](./get_width/)() | يحصل على عرض الإطار المحدد، بالنقاط. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## ملاحظات


يتم دائمًا إنشاء هذا الكائن. إذا كانت الفقرة إطارًا، فستحتوي جميع الخصائص على القيم المناسبة، وإلا سيتم تعيين جميع الخصائص إلى القيم الافتراضية.

استخدم [IsFrame](./get_isframe/) للتحقق مما إذا كانت الفقرة إطارًا.

## أمثلة



يظهر كيفية الحصول على معلومات حول خصائص تنسيق الفقرات التي هي إطارات.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Paragraph frame.docx");

System::SharedPtr<Aspose::Words::Paragraph> paragraphFrame = doc->get_FirstSection()->get_Body()->get_Paragraphs()->LINQ_OfType<System::SharedPtr<Aspose::Words::Paragraph> >()->LINQ_First(static_cast<System::Func<System::SharedPtr<Aspose::Words::Paragraph>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Paragraph> p)>>([](System::SharedPtr<Aspose::Words::Paragraph> p) -> bool
{
    return p->get_FrameFormat()->get_IsFrame();
})));

ASPOSE_ASSERT_EQ(233.3, paragraphFrame->get_FrameFormat()->get_Width());
ASPOSE_ASSERT_EQ(138.8, paragraphFrame->get_FrameFormat()->get_Height());
ASSERT_EQ(Aspose::Words::HeightRule::AtLeast, paragraphFrame->get_FrameFormat()->get_HeightRule());
ASSERT_EQ(Aspose::Words::Drawing::HorizontalAlignment::Default, paragraphFrame->get_FrameFormat()->get_HorizontalAlignment());
ASSERT_EQ(Aspose::Words::Drawing::VerticalAlignment::Default, paragraphFrame->get_FrameFormat()->get_VerticalAlignment());
ASPOSE_ASSERT_EQ(34.05, paragraphFrame->get_FrameFormat()->get_HorizontalPosition());
ASSERT_EQ(Aspose::Words::Drawing::RelativeHorizontalPosition::Page, paragraphFrame->get_FrameFormat()->get_RelativeHorizontalPosition());
ASPOSE_ASSERT_EQ(9.0, paragraphFrame->get_FrameFormat()->get_HorizontalDistanceFromText());
ASPOSE_ASSERT_EQ(20.5, paragraphFrame->get_FrameFormat()->get_VerticalPosition());
ASSERT_EQ(Aspose::Words::Drawing::RelativeVerticalPosition::Paragraph, paragraphFrame->get_FrameFormat()->get_RelativeVerticalPosition());
ASPOSE_ASSERT_EQ(0.0, paragraphFrame->get_FrameFormat()->get_VerticalDistanceFromText());
```

## انظر أيضًا

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
