---
title: "Aspose::Words::Document::get_FontSettings method"
linktitle: "get_FontSettings"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Document::get_FontSettings. يحصل على إعدادات خطوط المستند أو يضبطها في C++."
type: docs
weight: 25000
url: /ar/cpp/aspose.words/document/get_fontsettings/
---
## Document::get_FontSettings method


يحصل أو يضبط إعدادات خط المستند.

```cpp
System::SharedPtr<Aspose::Words::Fonts::FontSettings> Aspose::Words::Document::get_FontSettings() const
```

## ملاحظات


تسمح هذه الخاصية بتحديد إعدادات الخط لكل مستند. إذا تم تعيينها إلى **null**، سيتم استخدام إعدادات الخط الثابتة الافتراضية [DefaultInstance](../../../aspose.words.fonts/fontsettings/get_defaultinstance/).

القيمة الافتراضية هي **null**.

## أمثلة



يوضح كيفية تعيين قواعد استبدال الخطوط.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Name(u"Arial");
builder->Writeln(u"Hello world!");
builder->get_Font()->set_Name(u"Amethysta");
builder->Writeln(u"The quick brown fox jumps over the lazy dog.");

System::ArrayPtr<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>> fontSources = Aspose::Words::Fonts::FontSettings::get_DefaultInstance()->GetFontsSources();

// مصادر الخطوط الافتراضية تحتوي على الخط الأول الذي يستخدمه المستند.
ASSERT_EQ(1, fontSources->get_Length());
ASSERT_TRUE(fontSources[0]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
{
    return f->get_FullFontName() == u"Arial";
}))));

// الخط الثاني، "Amethysta"، غير متوفر.
ASSERT_FALSE(fontSources[0]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
{
    return f->get_FullFontName() == u"Amethysta";
}))));

// يمكننا تكوين جدول استبدال الخطوط الذي يحدد
// أي الخطوط سيستخدمها Aspose.Words كبدائل للخطوط غير المتوفرة.
// حدد خطين بديلين للخط "Amethysta": "Arvo" و "Courier New".
// إذا كان البديل الأول غير متوفر، تحاول Aspose.Words استخدام البديل الثاني، وهكذا.
doc->set_FontSettings(System::MakeObject<Aspose::Words::Fonts::FontSettings>());
doc->get_FontSettings()->get_SubstitutionSettings()->get_TableSubstitution()->SetSubstitutes(u"Amethysta", System::MakeArray<System::String>({u"Arvo", u"Courier New"}));

// "Amethysta" غير متوفر، وتحدد قاعدة الاستبدال أن الخط الأول لاستخدامه كبديل هو "Arvo".
ASSERT_FALSE(fontSources[0]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
{
    return f->get_FullFontName() == u"Arvo";
}))));

// "Arvo" غير متوفر أيضًا، لكن "Courier New" متوفر.
ASSERT_TRUE(fontSources[0]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
{
    return f->get_FullFontName() == u"Courier New";
}))));

// ستعرض وثيقة الإخراج النص الذي يستخدم خط "Amethysta" منسقًا بخط "Courier New".
doc->Save(get_ArtifactsDir() + u"FontSettings.TableSubstitution.pdf");
```

## انظر أيضًا

* Class [FontSettings](../../../aspose.words.fonts/fontsettings/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
