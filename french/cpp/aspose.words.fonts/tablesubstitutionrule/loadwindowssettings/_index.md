---
title: "Aspose::Words::Fonts::TableSubstitutionRule::LoadWindowsSettings méthode"
linktitle: "LoadWindowsSettings"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Fonts::TableSubstitutionRule::LoadWindowsSettings méthode. Charge les paramètres de substitution de tableau prédéfinis pour la plateforme Windows en C++."
type: docs
weight: 9000
url: /fr/cpp/aspose.words.fonts/tablesubstitutionrule/loadwindowssettings/
---
## TableSubstitutionRule::LoadWindowsSettings method


Charge les paramètres de substitution de table prédéfinis pour la plateforme Windows.

```cpp
void Aspose::Words::Fonts::TableSubstitutionRule::LoadWindowsSettings()
```


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

* Class [TableSubstitutionRule](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
