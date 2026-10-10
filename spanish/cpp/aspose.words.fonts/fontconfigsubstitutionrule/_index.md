---
title: "Aspose::Words::Fonts::FontConfigSubstitutionRule clase"
linktitle: "FontConfigSubstitutionRule"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Fonts::FontConfigSubstitutionRule clase. Regla de sustitución de configuración de fuentes. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 4000
url: /es/cpp/aspose.words.fonts/fontconfigsubstitutionrule/
---
## FontConfigSubstitutionRule class


[Font](../../aspose.words/font/) config substitution rule. To learn more, visit the [Working with Fonts](https://docs.aspose.com/words/cpp/working-with-fonts/) documentation article.

```cpp
class FontConfigSubstitutionRule : public Aspose::Words::Fonts::FontSubstitutionRule
```

## Métodos

| Método | Descripción |
| --- | --- |
| virtual [get_Enabled](../fontsubstitutionrule/get_enabled/)() | Especifica si la regla está habilitada o no. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [IsFontConfigAvailable](./isfontconfigavailable/)() | Compruebe si la utilidad fontconfig está disponible o no. |
| [ResetCache](./resetcache/)() | Restablece la caché de los resultados de llamadas a fontconfig. |
| [set_Enabled](./set_enabled/)(bool) override | Especifica si la regla está habilitada o no. |
| static [Type](./type/)() |  |
## Observaciones


Esta regla utiliza la utilidad fontconfig en plataformas Linux (y otras similares a Unix) para obtener la sustitución si la fuente original no está disponible.

Si la utilidad fontconfig no está disponible, esta regla será ignorada.

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

* Class [FontSubstitutionRule](../fontsubstitutionrule/)
* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
