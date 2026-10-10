---
title: "طريقة Aspose::Words::Fonts::TableSubstitutionRule::SetSubstitutes"
linktitle: "SetSubstitutes"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Fonts::TableSubstitutionRule::SetSubstitutes. استبدل أسماء الخطوط البديلة للخط الأصلي المحدد في C++."
type: docs
weight: 11000
url: /ar/cpp/aspose.words.fonts/tablesubstitutionrule/setsubstitutes/
---
## TableSubstitutionRule::SetSubstitutes method


تجاوز أسماء الخطوط البديلة لاسم الخط الأصلي المحدد.

```cpp
void Aspose::Words::Fonts::TableSubstitutionRule::SetSubstitutes(const System::String &originalFontName, const System::ArrayPtr<System::String> &substituteFontNames)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| originalFontName | const System::String\& | اسم الخط الأصلي. |
| substituteFontNames | const System::ArrayPtr\<System::String\>\& | قائمة بأسماء الخطوط البديلة. |

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


يوضح كيفية العمل مع جداول استبدال الخطوط المخصصة.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto fontSettings = System::MakeObject<Aspose::Words::Fonts::FontSettings>();
doc->set_FontSettings(fontSettings);

// أنشئ قاعدة استبدال جدول جديدة وحمّل جدول استبدال الخطوط الافتراضي لنظام Windows.
System::SharedPtr<Aspose::Words::Fonts::TableSubstitutionRule> tableSubstitutionRule = fontSettings->get_SubstitutionSettings()->get_TableSubstitution();

// إذا اخترنا الخطوط حصريًا من مجلدنا، سنحتاج إلى جدول استبدال مخصص.
// لن نتمكن بعد الآن من الوصول إلى خطوط Microsoft Windows،
// مثل \"Arial\" أو \"Times New Roman\" لأنها غير موجودة في مجلد الخطوط الجديد لدينا.
auto folderFontSource = System::MakeObject<Aspose::Words::Fonts::FolderFontSource>(get_FontsDir(), false);
fontSettings->SetFontsSources(System::MakeArray<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>>({folderFontSource}));

// أدناه طريقتان لتحميل جدول الاستبدال من ملف في نظام الملفات المحلي.
// 1 -  من تدفق:
{
    auto fileStream = System::MakeObject<System::IO::FileStream>(get_MyDir() + u"Font substitution rules.xml", System::IO::FileMode::Open);
    tableSubstitutionRule->Load(fileStream);
}

// 2 -  مباشرةً من ملف:
tableSubstitutionRule->Load(get_MyDir() + u"Font substitution rules.xml");

// بما أننا لم نعد نمتلك إمكانية الوصول إلى \"Arial\"، سيحاول جدول الخطوط أولاً استبداله بـ \"Nonexistent Font\".
// لا نمتلك هذا الخط لذا سيتحول إلى الاستبدال التالي، \"Kreon\"، الموجود في مجلد \"MyFonts\".
ASPOSE_ASSERT_EQ(System::MakeArray<System::String>({u"Missing Font", u"Kreon"}), tableSubstitutionRule->GetSubstitutes(u"Arial")->LINQ_ToArray());

// يمكننا توسيع هذا الجدول برمجياً. سنضيف مدخلاً يستبدل \"Times New Roman\" بـ \"Arvo\".
ASSERT_TRUE(System::TestTools::IsNull(tableSubstitutionRule->GetSubstitutes(u"Times New Roman")));
tableSubstitutionRule->AddSubstitutes(u"Times New Roman", System::MakeArray<System::String>({u"Arvo"}));
ASPOSE_ASSERT_EQ(System::MakeArray<System::String>({u"Arvo"}), tableSubstitutionRule->GetSubstitutes(u"Times New Roman")->LINQ_ToArray());

// يمكننا إضافة استبدال احتياطي ثانوي لمدخل خط موجود باستخدام AddSubstitutes().
// في حال عدم توفر \"Arvo\"، سيبحث جدولنا عن \"M+ 2m\" كخيار استبدال ثانٍ.
tableSubstitutionRule->AddSubstitutes(u"Times New Roman", System::MakeArray<System::String>({u"M+ 2m"}));
ASPOSE_ASSERT_EQ(System::MakeArray<System::String>({u"Arvo", u"M+ 2m"}), tableSubstitutionRule->GetSubstitutes(u"Times New Roman")->LINQ_ToArray());

// يمكن لـ SetSubstitutes() تعيين قائمة جديدة من الخطوط البديلة لخط معين.
tableSubstitutionRule->SetSubstitutes(u"Times New Roman", System::MakeArray<System::String>({u"Squarish Sans CT", u"M+ 2m"}));
ASPOSE_ASSERT_EQ(System::MakeArray<System::String>({u"Squarish Sans CT", u"M+ 2m"}), tableSubstitutionRule->GetSubstitutes(u"Times New Roman")->LINQ_ToArray());

// كتابة النص بخطوط لا نمتلك إمكانية الوصول إليها سيؤدي إلى تطبيق قواعد الاستبدال الخاصة بنا.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->get_Font()->set_Name(u"Arial");
builder->Writeln(u"Text written in Arial, to be substituted by Kreon.");

builder->get_Font()->set_Name(u"Times New Roman");
builder->Writeln(u"Text written in Times New Roman, to be substituted by Squarish Sans CT.");

doc->Save(get_ArtifactsDir() + u"FontSettings.TableSubstitutionRule.Custom.pdf");
```

## انظر أيضًا

* Class [TableSubstitutionRule](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
