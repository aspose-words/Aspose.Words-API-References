---
title: "Aspose::Words::Fonts::FontSubstitutionSettings::get_FontConfigSubstitution метод"
linktitle: "get_FontConfigSubstitution"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Fonts::FontSubstitutionSettings::get_FontConfigSubstitution метод. Параметры, связанные с правилом замены конфигурации шрифта в C++."
type: docs
weight: 3000
url: /ru/cpp/aspose.words.fonts/fontsubstitutionsettings/get_fontconfigsubstitution/
---
## FontSubstitutionSettings::get_FontConfigSubstitution method


[Settings](../../../aspose.words.settings/) related to font config substitution rule.

```cpp
const System::SharedPtr<Aspose::Words::Fonts::FontConfigSubstitutionRule> & Aspose::Words::Fonts::FontSubstitutionSettings::get_FontConfigSubstitution() const
```


## Примеры



Показывает зависимую от операционной системы замену конфигурации шрифтов.
```cpp
auto fontSettings = System::MakeObject<Aspose::Words::Fonts::FontSettings>();
System::SharedPtr<Aspose::Words::Fonts::FontConfigSubstitutionRule> fontConfigSubstitution = fontSettings->get_SubstitutionSettings()->get_FontConfigSubstitution();

bool isWindows = System::MakeArray<System::PlatformID>({System::PlatformID::Win32NT, System::PlatformID::Win32S, System::PlatformID::Win32Windows, System::PlatformID::WinCE})->LINQ_Any(static_cast<System::Func<System::PlatformID, bool>>(static_cast<std::function<bool(System::PlatformID p)>>([](System::PlatformID p) -> bool
{
    return System::Environment::get_OSVersion().get_Platform() == p;
})));

// Объект FontConfigSubstitutionRule работает по‑разному на платформах Windows и не‑Windows.
// На Windows он недоступен.
if (isWindows)
{
    ASSERT_FALSE(fontConfigSubstitution->get_Enabled());
    ASSERT_FALSE(fontConfigSubstitution->IsFontConfigAvailable());
}

bool isLinuxOrMac = System::MakeArray<System::PlatformID>({System::PlatformID::Unix, System::PlatformID::MacOSX})->LINQ_Any(static_cast<System::Func<System::PlatformID, bool>>(static_cast<std::function<bool(System::PlatformID p)>>([](System::PlatformID p) -> bool
{
    return System::Environment::get_OSVersion().get_Platform() == p;
})));

// На Linux/Mac мы будем иметь к нему доступ и сможем выполнять операции.
if (isLinuxOrMac)
{
    ASSERT_TRUE(fontConfigSubstitution->get_Enabled());
    ASSERT_TRUE(fontConfigSubstitution->IsFontConfigAvailable());

    fontConfigSubstitution->ResetCache();
}
```

## См. также

* Class [FontConfigSubstitutionRule](../../fontconfigsubstitutionrule/)
* Class [FontSubstitutionSettings](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
