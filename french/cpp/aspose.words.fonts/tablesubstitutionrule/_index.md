---
title: "Aspose::Words::Fonts::TableSubstitutionRule classe"
linktitle: "TableSubstitutionRule"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Fonts::TableSubstitutionRule classe. Règle de substitution de police de tableau. Pour en savoir plus, consultez l’article de documentation en C++."
type: docs
weight: 18000
url: /fr/cpp/aspose.words.fonts/tablesubstitutionrule/
---
## TableSubstitutionRule class


Règle de substitution de police du tableau. Pour en savoir plus, consultez l'article de documentation [Working with Fonts](https://docs.aspose.com/words/cpp/working-with-fonts/).

```cpp
class TableSubstitutionRule : public Aspose::Words::Fonts::FontSubstitutionRule
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [AddSubstitutes](./addsubstitutes/)(const System::String\&, const System::ArrayPtr\<System::String\>\&) | Ajoute des noms de police de substitution pour le nom de police original donné. |
| virtual [get_Enabled](../fontsubstitutionrule/get_enabled/)() | Spécifie si la règle est activée ou non. |
| [GetSubstitutes](./getsubstitutes/)(const System::String\&) | Renvoie un tableau contenant les noms de police de substitution pour le nom de police original spécifié. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Load](./load/)(const System::String\&) | Charge les paramètres de substitution de tableau à partir d’un fichier XML. |
| [Load](./load/)(const System::SharedPtr\<System::IO::Stream\>\&) | Charge les paramètres de substitution de tableau à partir d’un flux XML. |
| [LoadAndroidSettings](./loadandroidsettings/)() | Charge les paramètres de substitution de table prédéfinis pour la plateforme Android. |
| [LoadLinuxSettings](./loadlinuxsettings/)() | Charge les paramètres de substitution de table prédéfinis pour la plateforme Linux. |
| [LoadWindowsSettings](./loadwindowssettings/)() | Charge les paramètres de substitution de table prédéfinis pour la plateforme Windows. |
| [Save](./save/)(const System::String\&) | Enregistre les paramètres de substitution de table actuels dans un fichier. |
| [Save](./save/)(const System::SharedPtr\<System::IO::Stream\>\&) | Enregistre les paramètres de substitution de table actuels dans un flux. |
| virtual [set_Enabled](../fontsubstitutionrule/set_enabled/)(bool) | Définisseur pour [Aspose::Words::Fonts::FontSubstitutionRule::get_Enabled](../fontsubstitutionrule/get_enabled/). |
| [SetSubstitutes](./setsubstitutes/)(const System::String\&, const System::ArrayPtr\<System::String\>\&) | Remplace les noms de polices de substitution pour le nom de police original donné. |
| static [Type](./type/)() |  |

## Exemples



Montre comment accéder aux tables de substitution de polices pour Windows et Linux.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto fontSettings = System::MakeObject<Aspose::Words::Fonts::FontSettings>();
doc->set_FontSettings(fontSettings);

// Crée une nouvelle règle de substitution de table et charge la table de substitution de polices Microsoft Windows par défaut.
System::SharedPtr<Aspose::Words::Fonts::TableSubstitutionRule> tableSubstitutionRule = fontSettings->get_SubstitutionSettings()->get_TableSubstitution();
tableSubstitutionRule->LoadWindowsSettings();

// Sous Windows, le substitut par défaut pour la police "Times New Roman CE" est "Times New Roman".
ASPOSE_ASSERT_EQ(System::MakeArray<System::String>({u"Times New Roman"}), tableSubstitutionRule->GetSubstitutes(u"Times New Roman CE")->LINQ_ToArray());

// Nous pouvons enregistrer la table sous forme de document XML.
tableSubstitutionRule->Save(get_ArtifactsDir() + u"FontSettings.TableSubstitutionRule.Windows.xml");

// Linux possède sa propre table de substitution.
// Il existe plusieurs polices de substitution pour "Times New Roman CE".
// Si le premier substitut, "FreeSerif", est également indisponible,
// cette règle parcourra les autres dans le tableau jusqu'à en trouver un disponible.
tableSubstitutionRule->LoadLinuxSettings();
ASPOSE_ASSERT_EQ(System::MakeArray<System::String>({u"FreeSerif", u"Liberation Serif", u"DejaVu Serif"}), tableSubstitutionRule->GetSubstitutes(u"Times New Roman CE")->LINQ_ToArray());

// Enregistrez la table de substitution Linux sous forme de document XML en utilisant un flux.
{
    auto fileStream = System::MakeObject<System::IO::FileStream>(get_ArtifactsDir() + u"FontSettings.TableSubstitutionRule.Linux.xml", System::IO::FileMode::Create);
    tableSubstitutionRule->Save(fileStream);
}
```

## Voir aussi

* Class [FontSubstitutionRule](../fontsubstitutionrule/)
* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
