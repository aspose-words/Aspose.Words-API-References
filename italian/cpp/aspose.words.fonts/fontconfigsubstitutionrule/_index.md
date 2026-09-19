---
title: "Aspose::Words::Fonts::FontConfigSubstitutionRule classe"
linktitle: "FontConfigSubstitutionRule"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Fonts::FontConfigSubstitutionRule classe. Regola di sostituzione della configurazione dei caratteri. Per saperne di più, visita l'articolo della documentazione in C++."
type: docs
weight: 4000
url: /it/cpp/aspose.words.fonts/fontconfigsubstitutionrule/
---
## FontConfigSubstitutionRule class


[Font](../../aspose.words/font/) config substitution rule. To learn more, visit the [Working with Fonts](https://docs.aspose.com/words/cpp/working-with-fonts/) documentation article.

```cpp
class FontConfigSubstitutionRule : public Aspose::Words::Fonts::FontSubstitutionRule
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| virtual [get_Enabled](../fontsubstitutionrule/get_enabled/)() | Specifica se la regola è abilitata o meno. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [IsFontConfigAvailable](./isfontconfigavailable/)() | Verifica se l'utilità fontconfig è disponibile o meno. |
| [ResetCache](./resetcache/)() | Reimposta la cache dei risultati delle chiamate a fontconfig. |
| [set_Enabled](./set_enabled/)(bool) override | Specifica se la regola è abilitata o meno. |
| static [Type](./type/)() |  |
## Note


Questa regola utilizza l'utilità fontconfig su piattaforme Linux (e altre simili a Unix) per ottenere la sostituzione se il carattere originale non è disponibile.

Se l'utilità fontconfig non è disponibile, questa regola verrà ignorata.

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

* Class [FontSubstitutionRule](../fontsubstitutionrule/)
* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
