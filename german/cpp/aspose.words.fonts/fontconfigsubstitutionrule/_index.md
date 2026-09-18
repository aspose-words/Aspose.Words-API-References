---
title: "Aspose::Words::Fonts::FontConfigSubstitutionRule Klasse"
linktitle: "FontConfigSubstitutionRule"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Fonts::FontConfigSubstitutionRule Klasse. Font-Konfigurations-Substitutionsregel. Weitere Informationen finden Sie im Dokumentationsartikel in C++."
type: docs
weight: 4000
url: /de/cpp/aspose.words.fonts/fontconfigsubstitutionrule/
---
## FontConfigSubstitutionRule class


[Font](../../aspose.words/font/) config substitution rule. To learn more, visit the [Working with Fonts](https://docs.aspose.com/words/cpp/working-with-fonts/) documentation article.

```cpp
class FontConfigSubstitutionRule : public Aspose::Words::Fonts::FontSubstitutionRule
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| virtual [get_Enabled](../fontsubstitutionrule/get_enabled/)() | Gibt an, ob die Regel aktiviert ist oder nicht. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [IsFontConfigAvailable](./isfontconfigavailable/)() | Prüfen Sie, ob das fontconfig-Dienstprogramm verfügbar ist oder nicht. |
| [ResetCache](./resetcache/)() | Setzt den Cache der fontconfig-Aufrufresultate zurück. |
| [set_Enabled](./set_enabled/)(bool) override | Gibt an, ob die Regel aktiviert ist oder nicht. |
| static [Type](./type/)() |  |
## Hinweise


Diese Regel verwendet das fontconfig-Dienstprogramm auf Linux (und anderen Unix-ähnlichen) Plattformen, um die Substitution zu erhalten, wenn die Originalschriftart nicht verfügbar ist.

Wenn das fontconfig-Dienstprogramm nicht verfügbar ist, wird diese Regel ignoriert.

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

* Class [FontSubstitutionRule](../fontsubstitutionrule/)
* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
