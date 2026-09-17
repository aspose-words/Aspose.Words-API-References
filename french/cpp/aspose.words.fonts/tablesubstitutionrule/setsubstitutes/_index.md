---
title: "Méthode Aspose::Words::Fonts::TableSubstitutionRule::SetSubstitutes"
linktitle: "SetSubstitutes"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Fonts::TableSubstitutionRule::SetSubstitutes. Remplace les noms de polices de substitution pour le nom de police original donné en C++."
type: docs
weight: 11000
url: /fr/cpp/aspose.words.fonts/tablesubstitutionrule/setsubstitutes/
---
## TableSubstitutionRule::SetSubstitutes method


Remplace les noms de polices de substitution pour le nom de police original donné.

```cpp
void Aspose::Words::Fonts::TableSubstitutionRule::SetSubstitutes(const System::String &originalFontName, const System::ArrayPtr<System::String> &substituteFontNames)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| originalFontName | const System::String\& | Nom de police original. |
| substituteFontNames | const System::ArrayPtr\<System::String\>\& | Liste des noms de polices alternatifs. |

## Exemples



Montre comment définir les règles de substitution de polices.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Name(u"Arial");
builder->Writeln(u"Hello world!");
builder->get_Font()->set_Name(u"Amethysta");
builder->Writeln(u"The quick brown fox jumps over the lazy dog.");

System::ArrayPtr<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>> fontSources = Aspose::Words::Fonts::FontSettings::get_DefaultInstance()->GetFontsSources();

// Les sources de polices par défaut contiennent la première police utilisée par le document.
ASSERT_EQ(1, fontSources->get_Length());
ASSERT_TRUE(fontSources[0]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
{
    return f->get_FullFontName() == u"Arial";
}))));

// La deuxième police, "Amethysta", n'est pas disponible.
ASSERT_FALSE(fontSources[0]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
{
    return f->get_FullFontName() == u"Amethysta";
}))));

// Nous pouvons configurer une table de substitution de polices qui détermine
// quelles polices Aspose.Words utilisera comme substituts pour les polices indisponibles.
// Définissez deux polices de substitution pour "Amethysta" : "Arvo" et "Courier New".
// Si le premier substitut n'est pas disponible, Aspose.Words tente d'utiliser le deuxième substitut, et ainsi de suite.
doc->set_FontSettings(System::MakeObject<Aspose::Words::Fonts::FontSettings>());
doc->get_FontSettings()->get_SubstitutionSettings()->get_TableSubstitution()->SetSubstitutes(u"Amethysta", System::MakeArray<System::String>({u"Arvo", u"Courier New"}));

// "Amethysta" n'est pas disponible, et la règle de substitution indique que la première police à utiliser comme substitut est "Arvo".
ASSERT_FALSE(fontSources[0]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
{
    return f->get_FullFontName() == u"Arvo";
}))));

// "Arvo" n'est pas non plus disponible, mais "Courier New" l'est.
ASSERT_TRUE(fontSources[0]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
{
    return f->get_FullFontName() == u"Courier New";
}))));

// Le document de sortie affichera le texte qui utilise la police "Amethysta" formaté avec "Courier New".
doc->Save(get_ArtifactsDir() + u"FontSettings.TableSubstitution.pdf");
```


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
