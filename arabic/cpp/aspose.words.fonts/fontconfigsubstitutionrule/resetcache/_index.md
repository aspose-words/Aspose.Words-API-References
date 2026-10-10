---
title: "طريقة Aspose::Words::Fonts::FontConfigSubstitutionRule::ResetCache"
linktitle: "ResetCache"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Fonts::FontConfigSubstitutionRule::ResetCache. تعيد تعيين ذاكرة التخزين المؤقت لنتائج استدعاء fontconfig في C++."
type: docs
weight: 5000
url: /ar/cpp/aspose.words.fonts/fontconfigsubstitutionrule/resetcache/
---
## FontConfigSubstitutionRule::ResetCache method


يعيد ضبط ذاكرة التخزين المؤقت لنتائج استدعاء fontconfig.

```cpp
void Aspose::Words::Fonts::FontConfigSubstitutionRule::ResetCache()
```


## أمثلة



يعرض استبدال تكوين الخط المعتمد على نظام التشغيل.
```cpp
auto fontSettings = System::MakeObject<Aspose::Words::Fonts::FontSettings>();
System::SharedPtr<Aspose::Words::Fonts::FontConfigSubstitutionRule> fontConfigSubstitution = fontSettings->get_SubstitutionSettings()->get_FontConfigSubstitution();

bool isWindows = System::MakeArray<System::PlatformID>({System::PlatformID::Win32NT, System::PlatformID::Win32S, System::PlatformID::Win32Windows, System::PlatformID::WinCE})->LINQ_Any(static_cast<System::Func<System::PlatformID, bool>>(static_cast<std::function<bool(System::PlatformID p)>>([](System::PlatformID p) -> bool
{
    return System::Environment::get_OSVersion().get_Platform() == p;
})));

// كائن FontConfigSubstitutionRule يعمل بشكل مختلف على منصات Windows/غير Windows.
// على Windows، غير متاح.
if (isWindows)
{
    ASSERT_FALSE(fontConfigSubstitution->get_Enabled());
    ASSERT_FALSE(fontConfigSubstitution->IsFontConfigAvailable());
}

bool isLinuxOrMac = System::MakeArray<System::PlatformID>({System::PlatformID::Unix, System::PlatformID::MacOSX})->LINQ_Any(static_cast<System::Func<System::PlatformID, bool>>(static_cast<std::function<bool(System::PlatformID p)>>([](System::PlatformID p) -> bool
{
    return System::Environment::get_OSVersion().get_Platform() == p;
})));

// على Linux/Mac، سيكون لدينا إمكانية الوصول إليه، وسنتمكن من تنفيذ العمليات.
if (isLinuxOrMac)
{
    ASSERT_TRUE(fontConfigSubstitution->get_Enabled());
    ASSERT_TRUE(fontConfigSubstitution->IsFontConfigAvailable());

    fontConfigSubstitution->ResetCache();
}
```

## انظر أيضًا

* Class [FontConfigSubstitutionRule](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
