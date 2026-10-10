---
title: "Aspose::Words::Fonts::FontConfigSubstitutionRule::set_Enabled metodu"
linktitle: "set_Enabled"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fonts::FontConfigSubstitutionRule::set_Enabled metodu. Kuralın C++'ta etkin olup olmadığını belirtir."
type: docs
weight: 6000
url: /tr/cpp/aspose.words.fonts/fontconfigsubstitutionrule/set_enabled/
---
## FontConfigSubstitutionRule::set_Enabled method


Kuralın etkin olup olmadığını belirtir.

```cpp
void Aspose::Words::Fonts::FontConfigSubstitutionRule::set_Enabled(bool value) override
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
