---
title: "Aspose::Words::Fonts::FontSettings::SetFontsFolder method"
linktitle: "SetFontsFolder"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Fonts::FontSettings::SetFontsFolder method. يحدد المجلد الذي يبحث فيه Aspose.Words عن خطوط TrueType عند عرض المستندات أو تضمين الخطوط. هذا اختصار إلى SetFontsFolders() لتحديد دليل خط واحد فقط في C++."
type: docs
weight: 11000
url: /ar/cpp/aspose.words.fonts/fontsettings/setfontsfolder/
---
## FontSettings::SetFontsFolder method


يضبط المجلد الذي يبحث فيه Aspose.Words عن خطوط TrueType عند عرض المستندات أو دمج الخطوط. هذا اختصار إلى [SetFontsFolders()](../) لتعيين دليل خط واحد فقط.

```cpp
void Aspose::Words::Fonts::FontSettings::SetFontsFolder(const System::String &fontFolder, bool recursive)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| fontFolder | const System::String\& | المجلد الذي يحتوي على خطوط TrueType. |
| متكرر | bool | صحيح لفحص المجلدات المحددة للخطوط بشكل متكرر. |

## أمثلة



يظهر كيفية تعيين دليل مصدر الخط.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Name(u"Arvo");
builder->Writeln(u"Hello world!");
builder->get_Font()->set_Name(u"Amethysta");
builder->Writeln(u"The quick brown fox jumps over the lazy dog.");

// مصادر الخط لدينا لا تحتوي على الخط الذي استخدمناه للنص في هذا المستند.
// إذا استخدمنا إعدادات الخط هذه أثناء تصيير هذا المستند،
// ستطبق Aspose.Words خطًا احتياطيًا على النص الذي يحتوي على خط لا يمكن لـ Aspose.Words تحديد موقعه.
System::ArrayPtr<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>> originalFontSources = Aspose::Words::Fonts::FontSettings::get_DefaultInstance()->GetFontsSources();

ASSERT_EQ(1, originalFontSources->get_Length());
ASSERT_TRUE(originalFontSources[0]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
{
    return f->get_FullFontName() == u"Arial";
}))));

// مصادر الخط الافتراضية تفتقد الخطين الذين نستخدمهما في هذا المستند.
ASSERT_FALSE(originalFontSources[0]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
{
    return f->get_FullFontName() == u"Arvo";
}))));
ASSERT_FALSE(originalFontSources[0]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
{
    return f->get_FullFontName() == u"Amethysta";
}))));

// استخدم طريقة "SetFontsFolder" لتعيين دليل سيعمل كمصدر خط جديد.
// مرّر "false" كقيمة للمعامل "recursive" لتضمين الخطوط من جميع ملفات الخط الموجودة في الدليل
// الذي نمرره كالمعامل الأول، لكن دون تضمين أي خطوط في أي من المجلدات الفرعية لهذا الدليل.
// مرّر "true" كقيمة للمعامل "recursive" لتضمين جميع ملفات الخط في الدليل الذي نمرره
// كمعامل أول، بالإضافة إلى جميع الخطوط في مجلداته الفرعية.
Aspose::Words::Fonts::FontSettings::get_DefaultInstance()->SetFontsFolder(get_FontsDir(), recursive);

System::ArrayPtr<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>> newFontSources = Aspose::Words::Fonts::FontSettings::get_DefaultInstance()->GetFontsSources();

ASSERT_EQ(1, newFontSources->get_Length());
ASSERT_FALSE(newFontSources[0]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
{
    return f->get_FullFontName() == u"Arial";
}))));
ASSERT_TRUE(newFontSources[0]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
{
    return f->get_FullFontName() == u"Arvo";
}))));

// خط "Amethysta" موجود في مجلد فرعي من دليل الخط.
if (recursive)
{
    ASSERT_EQ(30, newFontSources[0]->GetAvailableFonts()->get_Count());
    ASSERT_TRUE(newFontSources[0]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
    {
        return f->get_FullFontName() == u"Amethysta";
    }))));
}
else
{
    ASSERT_EQ(18, newFontSources[0]->GetAvailableFonts()->get_Count());
    ASSERT_FALSE(newFontSources[0]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
    {
        return f->get_FullFontName() == u"Amethysta";
    }))));
}

doc->Save(get_ArtifactsDir() + u"FontSettings.SetFontsFolder.pdf");

// استعد مصادر الخط الأصلية.
Aspose::Words::Fonts::FontSettings::get_DefaultInstance()->SetFontsSources(originalFontSources);
```

## انظر أيضًا

* Class [FontSettings](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
