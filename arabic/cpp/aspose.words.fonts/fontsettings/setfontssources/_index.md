---
title: "Aspose::Words::Fonts::FontSettings::SetFontsSources method"
linktitle: "SetFontsSources"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Fonts::FontSettings::SetFontsSources method. يحدد المصادر التي يبحث فيها Aspose.Words عن خطوط TrueType عند عرض المستندات أو تضمين الخطوط في C++."
type: docs
weight: 13000
url: /ar/cpp/aspose.words.fonts/fontsettings/setfontssources/
---
## FontSettings::SetFontsSources(const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Fonts::FontSourceBase\>\>\&) method


يضبط المصادر التي يبحث فيها Aspose.Words عن خطوط TrueType عند عرض المستندات أو دمج الخطوط.

```cpp
void Aspose::Words::Fonts::FontSettings::SetFontsSources(const System::ArrayPtr<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>> &sources)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| sources | const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Fonts::FontSourceBase\>\>\& | مصفوفة من المصادر التي تحتوي على خطوط TrueType. |
## ملاحظات


بشكل افتراضي، يبحث Aspose.Words عن الخطوط المثبتة على النظام.

تعيين هذه الخاصية يعيد ضبط ذاكرة التخزين المؤقت لجميع الخطوط التي تم تحميلها مسبقًا.

## أمثلة



يظهر كيفية إضافة مصدر خط إلى مصادر الخط الحالية لدينا.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Name(u"Arial");
builder->Writeln(u"Hello world!");
builder->get_Font()->set_Name(u"Amethysta");
builder->Writeln(u"The quick brown fox jumps over the lazy dog.");
builder->get_Font()->set_Name(u"Junction Light");
builder->Writeln(u"The quick brown fox jumps over the lazy dog.");

System::ArrayPtr<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>> originalFontSources = Aspose::Words::Fonts::FontSettings::get_DefaultInstance()->GetFontsSources();

ASSERT_EQ(1, originalFontSources->get_Length());

ASSERT_TRUE(originalFontSources[0]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
{
    return f->get_FullFontName() == u"Arial";
}))));

// مصدر الخط الافتراضي يفتقد خطين نستخدمهما في مستندنا.
// عند حفظ هذا المستند، ستطبق Aspose.Words خطوطًا احتياطية على جميع النصوص المهيأة بخطوط غير قابلة للوصول.
ASSERT_FALSE(originalFontSources[0]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
{
    return f->get_FullFontName() == u"Amethysta";
}))));
ASSERT_FALSE(originalFontSources[0]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
{
    return f->get_FullFontName() == u"Junction Light";
}))));

// أنشئ مصدر خط من مجلد يحتوي على خطوط.
auto folderFontSource = System::MakeObject<Aspose::Words::Fonts::FolderFontSource>(get_FontsDir(), true);

// تطبيق مصفوفة جديدة من مصادر الخطوط التي تحتوي على مصادر الخطوط الأصلية، بالإضافة إلى خطوطنا المخصصة.
System::ArrayPtr<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>> updatedFontSources = System::MakeArray<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>>({originalFontSources[0], folderFontSource});
Aspose::Words::Fonts::FontSettings::get_DefaultInstance()->SetFontsSources(updatedFontSources);

// تحقق من أن Aspose.Words لديها إمكانية الوصول إلى جميع الخطوط المطلوبة قبل أن نقوم بتحويل المستند إلى PDF.
updatedFontSources = Aspose::Words::Fonts::FontSettings::get_DefaultInstance()->GetFontsSources();

ASSERT_TRUE(updatedFontSources[0]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
{
    return f->get_FullFontName() == u"Arial";
}))));
ASSERT_TRUE(updatedFontSources[1]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
{
    return f->get_FullFontName() == u"Amethysta";
}))));
ASSERT_TRUE(updatedFontSources[1]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
{
    return f->get_FullFontName() == u"Junction Light";
}))));

doc->Save(get_ArtifactsDir() + u"FontSettings.AddFontSource.pdf");

// استعد مصادر الخط الأصلية.
Aspose::Words::Fonts::FontSettings::get_DefaultInstance()->SetFontsSources(originalFontSources);
```

## انظر أيضًا

* Class [FontSourceBase](../../fontsourcebase/)
* Class [FontSettings](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
## FontSettings::SetFontsSources(const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Fonts::FontSourceBase\>\>\&, const System::SharedPtr\<System::IO::Stream\>\&) method


يضبط المصادر التي يبحث فيها Aspose.Words عن خطوط TrueType ويحمّل بالإضافة إلى ذلك ذاكرة التخزين المؤقت للبحث عن الخطوط التي تم حفظها مسبقًا.

```cpp
void Aspose::Words::Fonts::FontSettings::SetFontsSources(const System::ArrayPtr<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>> &sources, const System::SharedPtr<System::IO::Stream> &cacheInputStream)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| sources | const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Fonts::FontSourceBase\>\>\& | مصفوفة من المصادر التي تحتوي على خطوط TrueType. |
| cacheInputStream | const System::SharedPtr\<System::IO::Stream\>\& | دفق الإدخال مع ذاكرة بحث الخطوط المحفوظة. |
## ملاحظات


[Loading](../../../aspose.words.loading/) previously saved font search cache will speed up the font cache initialization process. It is especially useful when access to font sources is complicated (e.g. when fonts are loaded via network).

عند حفظ وتحميل ذاكرة بحث الخطوط، يتم التعرف على الخطوط في المصادر المقدمة عبر مفتاح الذاكرة. بالنسبة للخطوط في [SystemFontSource](../../systemfontsource/) و[FolderFontSource](../../folderfontsource/) يكون مفتاح الذاكرة هو مسار ملف الخط. بالنسبة لـ[MemoryFontSource](../../memoryfontsource/) و[StreamFontSource](../../streamfontsource/) يتم تعريف مفتاح الذاكرة في خصائص [CacheKey](../../memoryfontsource/get_cachekey/) و[CacheKey](../../streamfontsource/get_cachekey/) على التوالي. بالنسبة لـ[FileFontSource](../../filefontsource/) يكون مفتاح الذاكرة إما خاصية [CacheKey](../../filefontsource/get_cachekey/) أو مسار ملف إذا كانت [CacheKey](../../filefontsource/get_cachekey/) **null**.

يُوصى بشدة بتوفير نفس مصادر الخطوط عند تحميل الذاكرة كما كان الحال عند حفظها. أي تغييرات في مصادر الخطوط (مثل إضافة خطوط جديدة، نقل ملفات الخطوط أو تغيير مفتاح الذاكرة) قد تؤدي إلى حل غير دقيق للخطوط بواسطة Aspose.Words.

## انظر أيضًا

* Class [FontSourceBase](../../fontsourcebase/)
* Class [FontSettings](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
