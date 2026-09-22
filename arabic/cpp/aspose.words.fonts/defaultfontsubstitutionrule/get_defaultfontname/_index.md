---
title: "Aspose::Words::Fonts::DefaultFontSubstitutionRule::get_DefaultFontName method"
linktitle: "get_DefaultFontName"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Fonts::DefaultFontSubstitutionRule::get_DefaultFontName method. يحصل أو يضبط اسم الخط الافتراضي في C++."
type: docs
weight: 2000
url: /ar/cpp/aspose.words.fonts/defaultfontsubstitutionrule/get_defaultfontname/
---
## DefaultFontSubstitutionRule::get_DefaultFontName method


يحصل على أو يضبط اسم الخط الافتراضي.

```cpp
System::String Aspose::Words::Fonts::DefaultFontSubstitutionRule::get_DefaultFontName()
```

## ملاحظات


القيمة الافتراضية هي 'Times New Roman'.

## أمثلة



يوضح كيفية تحديد خط افتراضي.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Name(u"Arial");
builder->Writeln(u"Hello world!");
builder->get_Font()->set_Name(u"Arvo");
builder->Writeln(u"The quick brown fox jumps over the lazy dog.");

System::ArrayPtr<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>> fontSources = Aspose::Words::Fonts::FontSettings::get_DefaultInstance()->GetFontsSources();

// مصادر الخطوط التي يستخدمها المستند تحتوي على الخط "Arial"، ولكن ليس "Arvo".
ASSERT_EQ(1, fontSources->get_Length());
ASSERT_TRUE(fontSources[0]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
{
    return f->get_FullFontName() == u"Arial";
}))));
ASSERT_FALSE(fontSources[0]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
{
    return f->get_FullFontName() == u"Arvo";
}))));

// قم بتعيين الخاصية "DefaultFontName" إلى "Courier New" لتقوم بـ،
// أثناء عرض المستند، استخدم ذلك الخط في جميع الحالات عندما لا يتوفر خط آخر.
Aspose::Words::Fonts::FontSettings::get_DefaultInstance()->get_SubstitutionSettings()->get_DefaultFontSubstitution()->set_DefaultFontName(u"Courier New");

ASSERT_TRUE(fontSources[0]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
{
    return f->get_FullFontName() == u"Courier New";
}))));

// ستستخدم Aspose.Words الآن الخط الافتراضي بدلاً من أي خطوط مفقودة أثناء أي عمليات عرض.
doc->Save(get_ArtifactsDir() + u"FontSettings.DefaultFontName.pdf");
```


يعرض كيفية ضبط قاعدة استبدال الخط الافتراضي.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto fontSettings = System::MakeObject<Aspose::Words::Fonts::FontSettings>();
doc->set_FontSettings(fontSettings);

// احصل على قاعدة الاستبدال الافتراضية داخل FontSettings.
// ستستبدل هذه القاعدة جميع الخطوط المفقودة بـ "Times New Roman".
System::SharedPtr<Aspose::Words::Fonts::DefaultFontSubstitutionRule> defaultFontSubstitutionRule = fontSettings->get_SubstitutionSettings()->get_DefaultFontSubstitution();
ASSERT_TRUE(defaultFontSubstitutionRule->get_Enabled());
ASSERT_EQ(u"Times New Roman", defaultFontSubstitutionRule->get_DefaultFontName());

// عيّن بديل الخط الافتراضي إلى "Courier New".
defaultFontSubstitutionRule->set_DefaultFontName(u"Courier New");

// باستخدام مُنشئ المستند، أضف بعض النص بخط لا نمتلكه لنرى حدوث الاستبدال،
// ثم قم بتصدير النتيجة إلى ملف PDF.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Name(u"Missing Font");
builder->Writeln(u"Line written in a missing font, which will be substituted with Courier New.");

doc->Save(get_ArtifactsDir() + u"FontSettings.DefaultFontSubstitutionRule.pdf");
```

## انظر أيضًا

* Class [DefaultFontSubstitutionRule](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
