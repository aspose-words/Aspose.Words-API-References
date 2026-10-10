---
title: "Aspose::Words::Fonts::FontSubstitutionRule klass"
linktitle: "FontSubstitutionRule"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Fonts::FontSubstitutionRule klass. Detta är en abstrakt basklass för teckensnittssubstitutionsregeln. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 12000
url: /sv/cpp/aspose.words.fonts/fontsubstitutionrule/
---
## FontSubstitutionRule class


Detta är en abstrakt basklass för teckensnittssubstitutionsregeln. För att lära dig mer, besök dokumentationsartikeln [Working with Fonts](https://docs.aspose.com/words/cpp/working-with-fonts/).

```cpp
class FontSubstitutionRule : public System::Object
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| virtual [get_Enabled](./get_enabled/)() | Anger om regeln är aktiverad eller inte. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [set_Enabled](./set_enabled/)(bool) | Sättare för [Aspose::Words::Fonts::FontSubstitutionRule::get_Enabled](./get_enabled/). |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
