---
title: "Aspose::Words::Fonts::FontConfigSubstitutionRule::set_Enabled Methode"
linktitle: "set_Enabled"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Fonts::FontConfigSubstitutionRule::set_Enabled Methode. Gibt an, ob die Regel in C++ aktiviert ist oder nicht."
type: docs
weight: 6000
url: /de/cpp/aspose.words.fonts/fontconfigsubstitutionrule/set_enabled/
---
## FontConfigSubstitutionRule::set_Enabled method


Gibt an, ob die Regel aktiviert ist oder nicht.

```cpp
void Aspose::Words::Fonts::FontConfigSubstitutionRule::set_Enabled(bool value) override
```


## Beispiele



Zeigt betriebssystemabhängige Font-Konfigurations-Substitution an.
```cpp
auto fontSettings = System::MakeObject<Aspose::Words::Fonts::FontSettings>();
System::SharedPtr<Aspose::Words::Fonts::FontConfigSubstitutionRule> fontConfigSubstitution = fontSettings->get_SubstitutionSettings()->get_FontConfigSubstitution();

bool isWindows = System::MakeArray<System::PlatformID>({System::PlatformID::Win32NT, System::PlatformID::Win32S, System::PlatformID::Win32Windows, System::PlatformID::WinCE})->LINQ_Any(static_cast<System::Func<System::PlatformID, bool>>(static_cast<std::function<bool(System::PlatformID p)>>([](System::PlatformID p) -> bool
{
    return System::Environment::get_OSVersion().get_Platform() == p;
})));

// Das FontConfigSubstitutionRule-Objekt funktioniert auf Windows-/Nicht-Windows-Plattformen unterschiedlich.
// Unter Windows ist es nicht verfügbar.
if (isWindows)
{
    ASSERT_FALSE(fontConfigSubstitution->get_Enabled());
    ASSERT_FALSE(fontConfigSubstitution->IsFontConfigAvailable());
}

bool isLinuxOrMac = System::MakeArray<System::PlatformID>({System::PlatformID::Unix, System::PlatformID::MacOSX})->LINQ_Any(static_cast<System::Func<System::PlatformID, bool>>(static_cast<std::function<bool(System::PlatformID p)>>([](System::PlatformID p) -> bool
{
    return System::Environment::get_OSVersion().get_Platform() == p;
})));

// Unter Linux/Mac haben wir Zugriff darauf und können Vorgänge ausführen.
if (isLinuxOrMac)
{
    ASSERT_TRUE(fontConfigSubstitution->get_Enabled());
    ASSERT_TRUE(fontConfigSubstitution->IsFontConfigAvailable());

    fontConfigSubstitution->ResetCache();
}
```

## Siehe auch

* Class [FontConfigSubstitutionRule](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
