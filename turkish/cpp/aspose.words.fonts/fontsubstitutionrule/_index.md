---
title: "Aspose::Words::Fonts::FontSubstitutionRule class"
linktitle: "FontSubstitutionRule"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fonts::FontSubstitutionRule sınıfı. Bu, yazı tipi ikamesi kuralı için soyut bir temel sınıftır. Daha fazla bilgi için C++'taki belge makalesini ziyaret edin."
type: docs
weight: 12000
url: /tr/cpp/aspose.words.fonts/fontsubstitutionrule/
---
## FontSubstitutionRule class


Bu, yazı tipi ikame kuralı için soyut bir temel sınıftır. Daha fazla bilgi için, [Working with Fonts](https://docs.aspose.com/words/cpp/working-with-fonts/) dokümantasyon makalesini ziyaret edin.

```cpp
class FontSubstitutionRule : public System::Object
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| virtual [get_Enabled](./get_enabled/)() | Kuralın etkin olup olmadığını belirtir. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [set_Enabled](./set_enabled/)(bool) | Ayarlayıcı: [Aspose::Words::Fonts::FontSubstitutionRule::get_Enabled](./get_enabled/). |
| static [Type](./type/)() |  |

## Örnekler



İşletim sistemi bağımlı yazı tipi yapılandırma ikamesini gösterir.
```cpp
auto fontSettings = System::MakeObject<Aspose::Words::Fonts::FontSettings>();
System::SharedPtr<Aspose::Words::Fonts::FontConfigSubstitutionRule> fontConfigSubstitution = fontSettings->get_SubstitutionSettings()->get_FontConfigSubstitution();

bool isWindows = System::MakeArray<System::PlatformID>({System::PlatformID::Win32NT, System::PlatformID::Win32S, System::PlatformID::Win32Windows, System::PlatformID::WinCE})->LINQ_Any(static_cast<System::Func<System::PlatformID, bool>>(static_cast<std::function<bool(System::PlatformID p)>>([](System::PlatformID p) -> bool
{
    return System::Environment::get_OSVersion().get_Platform() == p;
})));

// FontConfigSubstitutionRule nesnesi Windows/Windows dışı platformlarda farklı çalışır.
// Windows'ta kullanılamaz.
if (isWindows)
{
    ASSERT_FALSE(fontConfigSubstitution->get_Enabled());
    ASSERT_FALSE(fontConfigSubstitution->IsFontConfigAvailable());
}

bool isLinuxOrMac = System::MakeArray<System::PlatformID>({System::PlatformID::Unix, System::PlatformID::MacOSX})->LINQ_Any(static_cast<System::Func<System::PlatformID, bool>>(static_cast<std::function<bool(System::PlatformID p)>>([](System::PlatformID p) -> bool
{
    return System::Environment::get_OSVersion().get_Platform() == p;
})));

// Linux/Mac'te ona erişebileceğiz ve işlemler yapabileceğiz.
if (isLinuxOrMac)
{
    ASSERT_TRUE(fontConfigSubstitution->get_Enabled());
    ASSERT_TRUE(fontConfigSubstitution->IsFontConfigAvailable());

    fontConfigSubstitution->ResetCache();
}
```

## Ayrıca Bakınız

* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
