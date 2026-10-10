---
title: "Aspose::Words::Fonts::SystemFontSource classe"
linktitle: "SystemFontSource"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Fonts::SystemFontSource classe. Représente toutes les polices TrueType installées sur le système. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 17000
url: /fr/cpp/aspose.words.fonts/systemfontsource/
---
## SystemFontSource class


Représente toutes les polices TrueType installées sur le système. Pour en savoir plus, consultez l'article de documentation [Working with Fonts](https://docs.aspose.com/words/cpp/working-with-fonts/).

```cpp
class SystemFontSource : public Aspose::Words::Fonts::FontSourceBase
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [get_Priority](../fontsourcebase/get_priority/)() const | Renvoie la priorité de la source de police. |
| [get_Type](./get_type/)() override | Renvoie le type de la source de police. |
| [get_WarningCallback](../fontsourcebase/get_warningcallback/)() const | Appelé lors du traitement de la source de police lorsqu'un problème est détecté pouvant entraîner une perte de fidélité du formatage. |
| [GetAvailableFonts](../fontsourcebase/getavailablefonts/)() | Renvoie la liste des polices disponibles via cette source. |
| static [GetSystemFontFolders](./getsystemfontfolders/)() | Renvoie les dossiers de polices du système ou un tableau vide si les dossiers ne sont pas accessibles. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_WarningCallback](../fontsourcebase/set_warningcallback/)(const System::SharedPtr\<Aspose::Words::IWarningCallback\>\&) | Appelé lors du traitement de la source de police lorsqu'un problème est détecté pouvant entraîner une perte de fidélité du formatage. |
| [SystemFontSource](./systemfontsource/)() | Constructeur. |
| [SystemFontSource](./systemfontsource/)(int32_t) | Constructeur. |
| static [Type](./type/)() |  |

## Exemples



Montre comment accéder à la source de polices système d'un document et définir des substituts de police.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
doc->set_FontSettings(System::MakeObject<Aspose::Words::Fonts::FontSettings>());

// Par défaut, un document vierge contient toujours une source de polices système.
ASSERT_EQ(1, doc->get_FontSettings()->GetFontsSources()->get_Length());

auto systemFontSource = System::ExplicitCast<Aspose::Words::Fonts::SystemFontSource>(doc->get_FontSettings()->GetFontsSources()->idx_get(0));
ASSERT_EQ(Aspose::Words::Fonts::FontSourceType::SystemFonts, systemFontSource->get_Type());
ASSERT_EQ(0, systemFontSource->get_Priority());

System::PlatformID pid = System::Environment::get_OSVersion().get_Platform();
bool isWindows = (pid == System::PlatformID::Win32NT) || (pid == System::PlatformID::Win32S) || (pid == System::PlatformID::Win32Windows) || (pid == System::PlatformID::WinCE);
if (isWindows)
{
    const System::String fontsPath = u"C:\\WINDOWS\\Fonts";
    System::String actual = System::Default<System::String>();
    System::String condExpression = Aspose::Words::Fonts::SystemFontSource::GetSystemFontFolders()->LINQ_FirstOrDefault();
    if (condExpression != nullptr)
    {
        actual = condExpression.ToLower();
    }
    ASSERT_EQ(fontsPath.ToLower(), actual);
}

for (System::String systemFontFolder : Aspose::Words::Fonts::SystemFontSource::GetSystemFontFolders())
{
    std::cout << systemFontFolder << std::endl;
}

// Définissez une police qui existe dans le répertoire Windows Fonts comme substitut d'une police qui n'existe pas.
doc->get_FontSettings()->get_SubstitutionSettings()->get_FontInfoSubstitution()->set_Enabled(true);
doc->get_FontSettings()->get_SubstitutionSettings()->get_TableSubstitution()->AddSubstitutes(u"Kreon-Regular", System::MakeArray<System::String>({u"Calibri"}));

ASSERT_EQ(1, doc->get_FontSettings()->get_SubstitutionSettings()->get_TableSubstitution()->GetSubstitutes(u"Kreon-Regular")->LINQ_Count());
ASSERT_TRUE(doc->get_FontSettings()->get_SubstitutionSettings()->get_TableSubstitution()->GetSubstitutes(u"Kreon-Regular")->LINQ_ToArray()->Contains(u"Calibri"));

// Alternativement, nous pourrions ajouter une source de police de dossier dans laquelle le dossier correspondant contient la police.
auto folderFontSource = System::MakeObject<Aspose::Words::Fonts::FolderFontSource>(get_FontsDir(), false);
doc->get_FontSettings()->SetFontsSources(System::MakeArray<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>>({systemFontSource, folderFontSource}));
ASSERT_EQ(2, doc->get_FontSettings()->GetFontsSources()->get_Length());

// Réinitialiser les sources de police nous laisse toujours la source de police système ainsi que nos substituts.
doc->get_FontSettings()->ResetFontSources();

ASSERT_EQ(1, doc->get_FontSettings()->GetFontsSources()->get_Length());
ASSERT_EQ(Aspose::Words::Fonts::FontSourceType::SystemFonts, doc->get_FontSettings()->GetFontsSources()->idx_get(0)->get_Type());
ASSERT_EQ(1, doc->get_FontSettings()->get_SubstitutionSettings()->get_TableSubstitution()->GetSubstitutes(u"Kreon-Regular")->LINQ_Count());
ASSERT_TRUE(doc->get_FontSettings()->get_SubstitutionSettings()->get_FontNameSubstitution()->get_Enabled());
```

## Voir aussi

* Class [FontSourceBase](../fontsourcebase/)
* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
