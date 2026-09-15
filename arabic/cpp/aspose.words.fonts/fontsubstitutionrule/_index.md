---
title: "فئة Aspose::Words::Fonts::FontSubstitutionRule"
linktitle: "FontSubstitutionRule"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "فئة Aspose::Words::Fonts::FontSubstitutionRule. هذه فئة أساسية مجردة لقاعدة استبدال الخط. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 12000
url: /ar/cpp/aspose.words.fonts/fontsubstitutionrule/
---
## FontSubstitutionRule class


هذه فئة أساسية مجردة لقاعدة استبدال الخط. لمزيد من المعلومات، قم بزيارة مقالة الوثائق [Working with Fonts](https://docs.aspose.com/words/cpp/working-with-fonts/).

```cpp
class FontSubstitutionRule : public System::Object
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| virtual [get_Enabled](./get_enabled/)() | يحدد ما إذا كانت القاعدة مفعّلة أم لا. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [set_Enabled](./set_enabled/)(bool) | مُعيّن لـ [Aspose::Words::Fonts::FontSubstitutionRule::get_Enabled](./get_enabled/). |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
