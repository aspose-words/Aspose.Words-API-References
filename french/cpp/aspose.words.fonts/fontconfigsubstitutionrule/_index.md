---
title: "Aspose::Words::Fonts::FontConfigSubstitutionRule class"
linktitle: "FontConfigSubstitutionRule"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Fonts::FontConfigSubstitutionRule class. Règle de substitution de configuration de police. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 4000
url: /fr/cpp/aspose.words.fonts/fontconfigsubstitutionrule/
---
## FontConfigSubstitutionRule class


[Font](../../aspose.words/font/) config substitution rule. To learn more, visit the [Working with Fonts](https://docs.aspose.com/words/cpp/working-with-fonts/) documentation article.

```cpp
class FontConfigSubstitutionRule : public Aspose::Words::Fonts::FontSubstitutionRule
```

## Méthodes

| Méthode | Description |
| --- | --- |
| virtual [get_Enabled](../fontsubstitutionrule/get_enabled/)() | Spécifie si la règle est activée ou non. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [IsFontConfigAvailable](./isfontconfigavailable/)() | Vérifiez si l'utilitaire fontconfig est disponible ou non. |
| [ResetCache](./resetcache/)() | Réinitialise le cache des résultats d'appel de fontconfig. |
| [set_Enabled](./set_enabled/)(bool) override | Spécifie si la règle est activée ou non. |
| static [Type](./type/)() |  |
## Remarques


Cette règle utilise l'utilitaire fontconfig sur les plateformes Linux (et autres de type Unix) pour obtenir la substitution si la police d'origine n'est pas disponible.

Si l'utilitaire fontconfig n'est pas disponible, cette règle sera ignorée.

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

* Class [FontSubstitutionRule](../fontsubstitutionrule/)
* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
