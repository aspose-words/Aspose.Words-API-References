---
title: "Aspose::Words::Fonts::FontSubstitutionRule class"
linktitle: "FontSubstitutionRule"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Fonts::FontSubstitutionRule class. Il s'agit d'une classe de base abstraite pour la règle de substitution de police. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 12000
url: /fr/cpp/aspose.words.fonts/fontsubstitutionrule/
---
## FontSubstitutionRule class


Il s'agit d'une classe de base abstraite pour la règle de substitution de police. Pour en savoir plus, consultez l'article de documentation [Working with Fonts](https://docs.aspose.com/words/cpp/working-with-fonts/).

```cpp
class FontSubstitutionRule : public System::Object
```

## Méthodes

| Méthode | Description |
| --- | --- |
| virtual [get_Enabled](./get_enabled/)() | Spécifie si la règle est activée ou non. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [set_Enabled](./set_enabled/)(bool) | Mutateur pour [Aspose::Words::Fonts::FontSubstitutionRule::get_Enabled](./get_enabled/). |
| static [Type](./type/)() |  |

## Exemples



Affiche la substitution de configuration de police dépendante du système d'exploitation.
```cpp
auto fontSettings = System::MakeObject<Aspose::Words::Fonts::FontSettings>();
System::SharedPtr<Aspose::Words::Fonts::FontConfigSubstitutionRule> fontConfigSubstitution = fontSettings->get_SubstitutionSettings()->get_FontConfigSubstitution();

bool isWindows = System::MakeArray<System::PlatformID>({System::PlatformID::Win32NT, System::PlatformID::Win32S, System::PlatformID::Win32Windows, System::PlatformID::WinCE})->LINQ_Any(static_cast<System::Func<System::PlatformID, bool>>(static_cast<std::function<bool(System::PlatformID p)>>([](System::PlatformID p) -> bool
{
    return System::Environment::get_OSVersion().get_Platform() == p;
})));

// L'objet FontConfigSubstitutionRule fonctionne différemment sur les plateformes Windows/non-Windows.
// Sur Windows, il n'est pas disponible.
if (isWindows)
{
    ASSERT_FALSE(fontConfigSubstitution->get_Enabled());
    ASSERT_FALSE(fontConfigSubstitution->IsFontConfigAvailable());
}

bool isLinuxOrMac = System::MakeArray<System::PlatformID>({System::PlatformID::Unix, System::PlatformID::MacOSX})->LINQ_Any(static_cast<System::Func<System::PlatformID, bool>>(static_cast<std::function<bool(System::PlatformID p)>>([](System::PlatformID p) -> bool
{
    return System::Environment::get_OSVersion().get_Platform() == p;
})));

// Sur Linux/Mac, nous y aurons accès et serons capables d'effectuer des opérations.
if (isLinuxOrMac)
{
    ASSERT_TRUE(fontConfigSubstitution->get_Enabled());
    ASSERT_TRUE(fontConfigSubstitution->IsFontConfigAvailable());

    fontConfigSubstitution->ResetCache();
}
```

## Voir aussi

* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
