---
title: "Aspose::Words::Document::get_FontSettings méthode"
linktitle: "get_FontSettings"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Document::get_FontSettings méthode. Obtient ou définit les paramètres de police du document en C++."
type: docs
weight: 25000
url: /fr/cpp/aspose.words/document/get_fontsettings/
---
## Document::get_FontSettings method


Obtient ou définit les paramètres de police du document.

```cpp
System::SharedPtr<Aspose::Words::Fonts::FontSettings> Aspose::Words::Document::get_FontSettings() const
```

## Remarques


Cette propriété permet de spécifier les paramètres de police par document. Si elle est définie sur **null**, les paramètres de police statiques par défaut [DefaultInstance](../../../aspose.words.fonts/fontsettings/get_defaultinstance/) seront utilisés.

La valeur par défaut est **null**.

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

## Voir aussi

* Class [FontSettings](../../../aspose.words.fonts/fontsettings/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
