---
title: "Aspose::Words::Fonts::FontConfigSubstitutionRule::IsFontConfigAvailable metodu"
linktitle: "IsFontConfigAvailable"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fonts::FontConfigSubstitutionRule::IsFontConfigAvailable metodu. C++'ta fontconfig yardımcı programının mevcut olup olmadığını kontrol eder."
type: docs
weight: 4000
url: /tr/cpp/aspose.words.fonts/fontconfigsubstitutionrule/isfontconfigavailable/
---
## FontConfigSubstitutionRule::IsFontConfigAvailable method


fontconfig aracının mevcut olup olmadığını kontrol edin.

```cpp
bool Aspose::Words::Fonts::FontConfigSubstitutionRule::IsFontConfigAvailable()
```


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

* Class [FontConfigSubstitutionRule](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
