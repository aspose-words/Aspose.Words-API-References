---
title: "Metodo IsFontConfigAvailable di Aspose::Words::Fonts::FontConfigSubstitutionRule"
linktitle: "IsFontConfigAvailable"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo IsFontConfigAvailable di Aspose::Words::Fonts::FontConfigSubstitutionRule. Verifica se l'utilità fontconfig è disponibile o meno in C++."
type: docs
weight: 4000
url: /it/cpp/aspose.words.fonts/fontconfigsubstitutionrule/isfontconfigavailable/
---
## FontConfigSubstitutionRule::IsFontConfigAvailable method


Verifica se l'utilità fontconfig è disponibile o meno.

```cpp
bool Aspose::Words::Fonts::FontConfigSubstitutionRule::IsFontConfigAvailable()
```


## Esempi



Mostra la sostituzione della configurazione dei caratteri dipendente dal sistema operativo.
```cpp
auto fontSettings = System::MakeObject<Aspose::Words::Fonts::FontSettings>();
System::SharedPtr<Aspose::Words::Fonts::FontConfigSubstitutionRule> fontConfigSubstitution = fontSettings->get_SubstitutionSettings()->get_FontConfigSubstitution();

bool isWindows = System::MakeArray<System::PlatformID>({System::PlatformID::Win32NT, System::PlatformID::Win32S, System::PlatformID::Win32Windows, System::PlatformID::WinCE})->LINQ_Any(static_cast<System::Func<System::PlatformID, bool>>(static_cast<std::function<bool(System::PlatformID p)>>([](System::PlatformID p) -> bool
{
    return System::Environment::get_OSVersion().get_Platform() == p;
})));

// L'oggetto FontConfigSubstitutionRule funziona diversamente su piattaforme Windows/non-Windows.
// Su Windows, non è disponibile.
if (isWindows)
{
    ASSERT_FALSE(fontConfigSubstitution->get_Enabled());
    ASSERT_FALSE(fontConfigSubstitution->IsFontConfigAvailable());
}

bool isLinuxOrMac = System::MakeArray<System::PlatformID>({System::PlatformID::Unix, System::PlatformID::MacOSX})->LINQ_Any(static_cast<System::Func<System::PlatformID, bool>>(static_cast<std::function<bool(System::PlatformID p)>>([](System::PlatformID p) -> bool
{
    return System::Environment::get_OSVersion().get_Platform() == p;
})));

// Su Linux/Mac, avremo accesso ad esso e saremo in grado di eseguire operazioni.
if (isLinuxOrMac)
{
    ASSERT_TRUE(fontConfigSubstitution->get_Enabled());
    ASSERT_TRUE(fontConfigSubstitution->IsFontConfigAvailable());

    fontConfigSubstitution->ResetCache();
}
```

## Vedi anche

* Class [FontConfigSubstitutionRule](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
