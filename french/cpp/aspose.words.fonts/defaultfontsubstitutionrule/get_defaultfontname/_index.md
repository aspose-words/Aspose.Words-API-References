---
title: "Aspose::Words::Fonts::DefaultFontSubstitutionRule::get_DefaultFontName méthode"
linktitle: "get_DefaultFontName"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Fonts::DefaultFontSubstitutionRule::get_DefaultFontName méthode. Obtient ou définit le nom de police par défaut en C++."
type: docs
weight: 2000
url: /fr/cpp/aspose.words.fonts/defaultfontsubstitutionrule/get_defaultfontname/
---
## DefaultFontSubstitutionRule::get_DefaultFontName method


Obtient ou définit le nom de police par défaut.

```cpp
System::String Aspose::Words::Fonts::DefaultFontSubstitutionRule::get_DefaultFontName()
```

## Remarques


La valeur par défaut est 'Times New Roman'.

## Exemples



Montre comment spécifier une police par défaut.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Name(u"Arial");
builder->Writeln(u"Hello world!");
builder->get_Font()->set_Name(u"Arvo");
builder->Writeln(u"The quick brown fox jumps over the lazy dog.");

System::ArrayPtr<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>> fontSources = Aspose::Words::Fonts::FontSettings::get_DefaultInstance()->GetFontsSources();

// Les sources de polices utilisées par le document contiennent la police "Arial", mais pas "Arvo".
ASSERT_EQ(1, fontSources->get_Length());
ASSERT_TRUE(fontSources[0]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
{
    return f->get_FullFontName() == u"Arial";
}))));
ASSERT_FALSE(fontSources[0]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
{
    return f->get_FullFontName() == u"Arvo";
}))));

// Définissez la propriété "DefaultFontName" sur "Courier New" pour,
// lors du rendu du document, appliquer cette police dans tous les cas lorsqu'une autre police n'est pas disponible.
Aspose::Words::Fonts::FontSettings::get_DefaultInstance()->get_SubstitutionSettings()->get_DefaultFontSubstitution()->set_DefaultFontName(u"Courier New");

ASSERT_TRUE(fontSources[0]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
{
    return f->get_FullFontName() == u"Courier New";
}))));

// Aspose.Words utilisera désormais la police par défaut à la place de toute police manquante lors de tout appel de rendu.
doc->Save(get_ArtifactsDir() + u"FontSettings.DefaultFontName.pdf");
```


Montre comment définir la règle de substitution de police par défaut.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto fontSettings = System::MakeObject<Aspose::Words::Fonts::FontSettings>();
doc->set_FontSettings(fontSettings);

// Obtenez la règle de substitution par défaut dans FontSettings.
// Cette règle remplacera toutes les polices manquantes par "Times New Roman".
System::SharedPtr<Aspose::Words::Fonts::DefaultFontSubstitutionRule> defaultFontSubstitutionRule = fontSettings->get_SubstitutionSettings()->get_DefaultFontSubstitution();
ASSERT_TRUE(defaultFontSubstitutionRule->get_Enabled());
ASSERT_EQ(u"Times New Roman", defaultFontSubstitutionRule->get_DefaultFontName());

// Définissez le substitut de police par défaut sur "Courier New".
defaultFontSubstitutionRule->set_DefaultFontName(u"Courier New");

// En utilisant un constructeur de document, ajoutez du texte dans une police que nous ne possédons pas afin de voir la substitution se produire,
// et puis rendez le résultat au format PDF.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Name(u"Missing Font");
builder->Writeln(u"Line written in a missing font, which will be substituted with Courier New.");

doc->Save(get_ArtifactsDir() + u"FontSettings.DefaultFontSubstitutionRule.pdf");
```

## Voir aussi

* Class [DefaultFontSubstitutionRule](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
