---
title: "Aspose::Words::Fonts::FontConfigSubstitutionRule klass"
linktitle: "FontConfigSubstitutionRule"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Fonts::FontConfigSubstitutionRule klass. Regel för teckensnittskonfigurationssubstitution. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 4000
url: /sv/cpp/aspose.words.fonts/fontconfigsubstitutionrule/
---
## FontConfigSubstitutionRule class


[Font](../../aspose.words/font/) config substitution rule. To learn more, visit the [Working with Fonts](https://docs.aspose.com/words/cpp/working-with-fonts/) documentation article.

```cpp
class FontConfigSubstitutionRule : public Aspose::Words::Fonts::FontSubstitutionRule
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| virtual [get_Enabled](../fontsubstitutionrule/get_enabled/)() | Anger om regeln är aktiverad eller inte. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [IsFontConfigAvailable](./isfontconfigavailable/)() | Kontrollera om fontconfig-verktyget är tillgängligt eller inte. |
| [ResetCache](./resetcache/)() | Återställer cachen för fontconfig-anropsresultat. |
| [set_Enabled](./set_enabled/)(bool) override | Anger om regeln är aktiverad eller inte. |
| static [Type](./type/)() |  |
## Anmärkningar


Denna regel använder fontconfig-verktyget på Linux (och andra Unix-liknande) plattformar för att få substitutionen om det ursprungliga teckensnittet inte är tillgängligt.

Om fontconfig-verktyget inte är tillgängligt kommer denna regel att ignoreras.

## Exempel



Visar operativsystemberoende teckensnittskonfigurationssubstitution.
```cpp
auto fontSettings = System::MakeObject<Aspose::Words::Fonts::FontSettings>();
System::SharedPtr<Aspose::Words::Fonts::FontConfigSubstitutionRule> fontConfigSubstitution = fontSettings->get_SubstitutionSettings()->get_FontConfigSubstitution();

bool isWindows = System::MakeArray<System::PlatformID>({System::PlatformID::Win32NT, System::PlatformID::Win32S, System::PlatformID::Win32Windows, System::PlatformID::WinCE})->LINQ_Any(static_cast<System::Func<System::PlatformID, bool>>(static_cast<std::function<bool(System::PlatformID p)>>([](System::PlatformID p) -> bool
{
    return System::Environment::get_OSVersion().get_Platform() == p;
})));

// FontConfigSubstitutionRule-objektet fungerar annorlunda på Windows/icke-Windows-plattformar.
// På Windows är den inte tillgänglig.
if (isWindows)
{
    ASSERT_FALSE(fontConfigSubstitution->get_Enabled());
    ASSERT_FALSE(fontConfigSubstitution->IsFontConfigAvailable());
}

bool isLinuxOrMac = System::MakeArray<System::PlatformID>({System::PlatformID::Unix, System::PlatformID::MacOSX})->LINQ_Any(static_cast<System::Func<System::PlatformID, bool>>(static_cast<std::function<bool(System::PlatformID p)>>([](System::PlatformID p) -> bool
{
    return System::Environment::get_OSVersion().get_Platform() == p;
})));

// På Linux/Mac kommer vi att ha åtkomst till den och kunna utföra operationer.
if (isLinuxOrMac)
{
    ASSERT_TRUE(fontConfigSubstitution->get_Enabled());
    ASSERT_TRUE(fontConfigSubstitution->IsFontConfigAvailable());

    fontConfigSubstitution->ResetCache();
}
```

## Se även

* Class [FontSubstitutionRule](../fontsubstitutionrule/)
* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
