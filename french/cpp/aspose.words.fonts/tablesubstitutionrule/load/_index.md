---
title: "Aspose::Words::Fonts::TableSubstitutionRule::Load méthode"
linktitle: "Charger"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Fonts::TableSubstitutionRule::Load méthode. Charge les paramètres de substitution de table à partir d'un flux XML en C++."
type: docs
weight: 6000
url: /fr/cpp/aspose.words.fonts/tablesubstitutionrule/load/
---
## TableSubstitutionRule::Load(const System::SharedPtr\<System::IO::Stream\>\&) method


Charge les paramètres de substitution de tableau à partir d’un flux XML.

```cpp
void Aspose::Words::Fonts::TableSubstitutionRule::Load(const System::SharedPtr<System::IO::Stream> &stream)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| flux | const System::SharedPtr\<System::IO::Stream\>\& | Flux d'entrée. |

## Exemples



Montre comment travailler avec des tables de substitution de polices personnalisées.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto fontSettings = System::MakeObject<Aspose::Words::Fonts::FontSettings>();
doc->set_FontSettings(fontSettings);

// Créez une nouvelle règle de substitution de table et chargez la table de substitution de polices Windows par défaut.
System::SharedPtr<Aspose::Words::Fonts::TableSubstitutionRule> tableSubstitutionRule = fontSettings->get_SubstitutionSettings()->get_TableSubstitution();

// Si nous sélectionnons les polices exclusivement depuis notre dossier, nous aurons besoin d'une table de substitution personnalisée.
// Nous n'aurons plus accès aux polices Microsoft Windows,
// comme "Arial" ou "Times New Roman" car ils n'existent pas dans notre nouveau dossier de polices.
auto folderFontSource = System::MakeObject<Aspose::Words::Fonts::FolderFontSource>(get_FontsDir(), false);
fontSettings->SetFontsSources(System::MakeArray<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>>({folderFontSource}));

// Voici deux façons de charger une table de substitution à partir d'un fichier sur le système de fichiers local.
// 1 -  À partir d'un flux :
{
    auto fileStream = System::MakeObject<System::IO::FileStream>(get_MyDir() + u"Font substitution rules.xml", System::IO::FileMode::Open);
    tableSubstitutionRule->Load(fileStream);
}

// 2 -  Directement à partir d'un fichier :
tableSubstitutionRule->Load(get_MyDir() + u"Font substitution rules.xml");

// Comme nous n'avons plus accès à "Arial", notre table de polices essaiera d'abord de le remplacer par "Nonexistent Font".
// Nous n'avons pas cette police, elle passera donc au substitut suivant, "Kreon", trouvé dans le dossier "MyFonts".
ASPOSE_ASSERT_EQ(System::MakeArray<System::String>({u"Missing Font", u"Kreon"}), tableSubstitutionRule->GetSubstitutes(u"Arial")->LINQ_ToArray());

// Nous pouvons étendre cette table de manière programmatique. Nous ajouterons une entrée qui remplace "Times New Roman" par "Arvo"
ASSERT_TRUE(System::TestTools::IsNull(tableSubstitutionRule->GetSubstitutes(u"Times New Roman")));
tableSubstitutionRule->AddSubstitutes(u"Times New Roman", System::MakeArray<System::String>({u"Arvo"}));
ASPOSE_ASSERT_EQ(System::MakeArray<System::String>({u"Arvo"}), tableSubstitutionRule->GetSubstitutes(u"Times New Roman")->LINQ_ToArray());

// Nous pouvons ajouter un substitut de secours secondaire pour une entrée de police existante avec AddSubstitutes().
// Dans le cas où "Arvo" n'est pas disponible, notre table recherchera "M+ 2m" comme deuxième option de substitution.
tableSubstitutionRule->AddSubstitutes(u"Times New Roman", System::MakeArray<System::String>({u"M+ 2m"}));
ASPOSE_ASSERT_EQ(System::MakeArray<System::String>({u"Arvo", u"M+ 2m"}), tableSubstitutionRule->GetSubstitutes(u"Times New Roman")->LINQ_ToArray());

// SetSubstitutes() peut définir une nouvelle liste de polices de substitution pour une police.
tableSubstitutionRule->SetSubstitutes(u"Times New Roman", System::MakeArray<System::String>({u"Squarish Sans CT", u"M+ 2m"}));
ASPOSE_ASSERT_EQ(System::MakeArray<System::String>({u"Squarish Sans CT", u"M+ 2m"}), tableSubstitutionRule->GetSubstitutes(u"Times New Roman")->LINQ_ToArray());

// Écrire du texte avec des polices auxquelles nous n'avons pas accès déclenchera nos règles de substitution.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->get_Font()->set_Name(u"Arial");
builder->Writeln(u"Text written in Arial, to be substituted by Kreon.");

builder->get_Font()->set_Name(u"Times New Roman");
builder->Writeln(u"Text written in Times New Roman, to be substituted by Squarish Sans CT.");

doc->Save(get_ArtifactsDir() + u"FontSettings.TableSubstitutionRule.Custom.pdf");
```

## Voir aussi

* Class [TableSubstitutionRule](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
## TableSubstitutionRule::Load(const System::String\&) method


Charge les paramètres de substitution de tableau à partir d’un fichier XML.

```cpp
void Aspose::Words::Fonts::TableSubstitutionRule::Load(const System::String &fileName)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| fileName | const System::String\& | Nom de fichier d'entrée. |

## Exemples



Montre comment travailler avec des tables de substitution de polices personnalisées.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto fontSettings = System::MakeObject<Aspose::Words::Fonts::FontSettings>();
doc->set_FontSettings(fontSettings);

// Créez une nouvelle règle de substitution de table et chargez la table de substitution de polices Windows par défaut.
System::SharedPtr<Aspose::Words::Fonts::TableSubstitutionRule> tableSubstitutionRule = fontSettings->get_SubstitutionSettings()->get_TableSubstitution();

// Si nous sélectionnons les polices exclusivement depuis notre dossier, nous aurons besoin d'une table de substitution personnalisée.
// Nous n'aurons plus accès aux polices Microsoft Windows,
// comme "Arial" ou "Times New Roman" car ils n'existent pas dans notre nouveau dossier de polices.
auto folderFontSource = System::MakeObject<Aspose::Words::Fonts::FolderFontSource>(get_FontsDir(), false);
fontSettings->SetFontsSources(System::MakeArray<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>>({folderFontSource}));

// Voici deux façons de charger une table de substitution à partir d'un fichier sur le système de fichiers local.
// 1 -  À partir d'un flux :
{
    auto fileStream = System::MakeObject<System::IO::FileStream>(get_MyDir() + u"Font substitution rules.xml", System::IO::FileMode::Open);
    tableSubstitutionRule->Load(fileStream);
}

// 2 -  Directement à partir d'un fichier :
tableSubstitutionRule->Load(get_MyDir() + u"Font substitution rules.xml");

// Comme nous n'avons plus accès à "Arial", notre table de polices essaiera d'abord de le remplacer par "Nonexistent Font".
// Nous n'avons pas cette police, elle passera donc au substitut suivant, "Kreon", trouvé dans le dossier "MyFonts".
ASPOSE_ASSERT_EQ(System::MakeArray<System::String>({u"Missing Font", u"Kreon"}), tableSubstitutionRule->GetSubstitutes(u"Arial")->LINQ_ToArray());

// Nous pouvons étendre cette table de manière programmatique. Nous ajouterons une entrée qui remplace "Times New Roman" par "Arvo"
ASSERT_TRUE(System::TestTools::IsNull(tableSubstitutionRule->GetSubstitutes(u"Times New Roman")));
tableSubstitutionRule->AddSubstitutes(u"Times New Roman", System::MakeArray<System::String>({u"Arvo"}));
ASPOSE_ASSERT_EQ(System::MakeArray<System::String>({u"Arvo"}), tableSubstitutionRule->GetSubstitutes(u"Times New Roman")->LINQ_ToArray());

// Nous pouvons ajouter un substitut de secours secondaire pour une entrée de police existante avec AddSubstitutes().
// Dans le cas où "Arvo" n'est pas disponible, notre table recherchera "M+ 2m" comme deuxième option de substitution.
tableSubstitutionRule->AddSubstitutes(u"Times New Roman", System::MakeArray<System::String>({u"M+ 2m"}));
ASPOSE_ASSERT_EQ(System::MakeArray<System::String>({u"Arvo", u"M+ 2m"}), tableSubstitutionRule->GetSubstitutes(u"Times New Roman")->LINQ_ToArray());

// SetSubstitutes() peut définir une nouvelle liste de polices de substitution pour une police.
tableSubstitutionRule->SetSubstitutes(u"Times New Roman", System::MakeArray<System::String>({u"Squarish Sans CT", u"M+ 2m"}));
ASPOSE_ASSERT_EQ(System::MakeArray<System::String>({u"Squarish Sans CT", u"M+ 2m"}), tableSubstitutionRule->GetSubstitutes(u"Times New Roman")->LINQ_ToArray());

// Écrire du texte avec des polices auxquelles nous n'avons pas accès déclenchera nos règles de substitution.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->get_Font()->set_Name(u"Arial");
builder->Writeln(u"Text written in Arial, to be substituted by Kreon.");

builder->get_Font()->set_Name(u"Times New Roman");
builder->Writeln(u"Text written in Times New Roman, to be substituted by Squarish Sans CT.");

doc->Save(get_ArtifactsDir() + u"FontSettings.TableSubstitutionRule.Custom.pdf");
```

## Voir aussi

* Class [TableSubstitutionRule](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
