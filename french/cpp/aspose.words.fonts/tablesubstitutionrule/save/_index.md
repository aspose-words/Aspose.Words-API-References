---
title: "Aspose::Words::Fonts::TableSubstitutionRule::Save méthode"
linktitle: "Save"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Fonts::TableSubstitutionRule::Save méthode. Enregistre les paramètres de substitution de tableau actuels dans le flux en C++."
type: docs
weight: 10000
url: /fr/cpp/aspose.words.fonts/tablesubstitutionrule/save/
---
## TableSubstitutionRule::Save(const System::SharedPtr\<System::IO::Stream\>\&) method


Enregistre les paramètres de substitution de table actuels dans un flux.

```cpp
void Aspose::Words::Fonts::TableSubstitutionRule::Save(const System::SharedPtr<System::IO::Stream> &outputStream)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Flux de sortie. |

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
## TableSubstitutionRule::Save(const System::String\&) method


Enregistre les paramètres de substitution de table actuels dans un fichier.

```cpp
void Aspose::Words::Fonts::TableSubstitutionRule::Save(const System::String &fileName)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| fileName | const System::String\& | Nom du fichier de sortie. |

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
