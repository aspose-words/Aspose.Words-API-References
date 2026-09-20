---
title: "Método Aspose::Words::Fonts::FontSubstitutionSettings::get_FontConfigSubstitution"
linktitle: "get_FontConfigSubstitution"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Fonts::FontSubstitutionSettings::get_FontConfigSubstitution. Configuraciones relacionadas con la regla de sustitución de configuración de fuente en C++."
type: docs
weight: 3000
url: /es/cpp/aspose.words.fonts/fontsubstitutionsettings/get_fontconfigsubstitution/
---
## FontSubstitutionSettings::get_FontConfigSubstitution method


[Settings](../../../aspose.words.settings/) related to font config substitution rule.

```cpp
const System::SharedPtr<Aspose::Words::Fonts::FontConfigSubstitutionRule> & Aspose::Words::Fonts::FontSubstitutionSettings::get_FontConfigSubstitution() const
```


## Ejemplos



Muestra la sustitución de configuración de fuentes dependiente del sistema operativo.
```cpp
auto fontSettings = System::MakeObject<Aspose::Words::Fonts::FontSettings>();
System::SharedPtr<Aspose::Words::Fonts::FontConfigSubstitutionRule> fontConfigSubstitution = fontSettings->get_SubstitutionSettings()->get_FontConfigSubstitution();

bool isWindows = System::MakeArray<System::PlatformID>({System::PlatformID::Win32NT, System::PlatformID::Win32S, System::PlatformID::Win32Windows, System::PlatformID::WinCE})->LINQ_Any(static_cast<System::Func<System::PlatformID, bool>>(static_cast<std::function<bool(System::PlatformID p)>>([](System::PlatformID p) -> bool
{
    return System::Environment::get_OSVersion().get_Platform() == p;
})));

// El objeto FontConfigSubstitutionRule funciona de manera diferente en plataformas Windows/no Windows.
// En Windows, no está disponible.
if (isWindows)
{
    ASSERT_FALSE(fontConfigSubstitution->get_Enabled());
    ASSERT_FALSE(fontConfigSubstitution->IsFontConfigAvailable());
}

bool isLinuxOrMac = System::MakeArray<System::PlatformID>({System::PlatformID::Unix, System::PlatformID::MacOSX})->LINQ_Any(static_cast<System::Func<System::PlatformID, bool>>(static_cast<std::function<bool(System::PlatformID p)>>([](System::PlatformID p) -> bool
{
    return System::Environment::get_OSVersion().get_Platform() == p;
})));

// En Linux/Mac, tendremos acceso a ella y podremos realizar operaciones.
if (isLinuxOrMac)
{
    ASSERT_TRUE(fontConfigSubstitution->get_Enabled());
    ASSERT_TRUE(fontConfigSubstitution->IsFontConfigAvailable());

    fontConfigSubstitution->ResetCache();
}
```

## Ver también

* Class [FontConfigSubstitutionRule](../../fontconfigsubstitutionrule/)
* Class [FontSubstitutionSettings](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
