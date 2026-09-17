---
title: "Aspose::Words::Fonts::FontSettings::GetFontsSources méthode"
linktitle: "GetFontsSources"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Fonts::FontSettings::GetFontsSources méthode. Obtient une copie du tableau contenant la liste des sources où Aspose.Words recherche les polices TrueType en C++."
type: docs
weight: 6000
url: /fr/cpp/aspose.words.fonts/fontsettings/getfontssources/
---
## FontSettings::GetFontsSources method


Obtient une copie du tableau contenant la liste des sources où Aspose.Words recherche les polices TrueType.

```cpp
System::ArrayPtr<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>> Aspose::Words::Fonts::FontSettings::GetFontsSources()
```


### ReturnValue

Une copie des sources de polices actuelles.
## Remarques


La valeur retournée est une copie des données utilisées par Aspose.Words. Si vous modifiez les entrées du tableau retourné, cela n'affectera pas le rendu du document. Pour spécifier de nouvelles sources de polices, utilisez la méthode [SetFontsSources()](../).

## Exemples



Montre comment ajouter une source de polices à nos sources de polices existantes.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Name(u"Arial");
builder->Writeln(u"Hello world!");
builder->get_Font()->set_Name(u"Amethysta");
builder->Writeln(u"The quick brown fox jumps over the lazy dog.");
builder->get_Font()->set_Name(u"Junction Light");
builder->Writeln(u"The quick brown fox jumps over the lazy dog.");

System::ArrayPtr<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>> originalFontSources = Aspose::Words::Fonts::FontSettings::get_DefaultInstance()->GetFontsSources();

ASSERT_EQ(1, originalFontSources->get_Length());

ASSERT_TRUE(originalFontSources[0]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
{
    return f->get_FullFontName() == u"Arial";
}))));

// La source de polices par défaut ne contient pas deux des polices que nous utilisons dans notre document.
// Lorsque nous enregistrons ce document, Aspose.Words appliquera des polices de secours à tout le texte formaté avec des polices inaccessibles.
ASSERT_FALSE(originalFontSources[0]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
{
    return f->get_FullFontName() == u"Amethysta";
}))));
ASSERT_FALSE(originalFontSources[0]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
{
    return f->get_FullFontName() == u"Junction Light";
}))));

// Créez une source de polices à partir d'un dossier qui contient des polices.
auto folderFontSource = System::MakeObject<Aspose::Words::Fonts::FolderFontSource>(get_FontsDir(), true);

// Appliquez un nouveau tableau de sources de polices qui contient les sources de polices d'origine, ainsi que nos polices personnalisées.
System::ArrayPtr<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>> updatedFontSources = System::MakeArray<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>>({originalFontSources[0], folderFontSource});
Aspose::Words::Fonts::FontSettings::get_DefaultInstance()->SetFontsSources(updatedFontSources);

// Vérifiez que Aspose.Words a accès à toutes les polices requises avant de rendre le document en PDF.
updatedFontSources = Aspose::Words::Fonts::FontSettings::get_DefaultInstance()->GetFontsSources();

ASSERT_TRUE(updatedFontSources[0]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
{
    return f->get_FullFontName() == u"Arial";
}))));
ASSERT_TRUE(updatedFontSources[1]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
{
    return f->get_FullFontName() == u"Amethysta";
}))));
ASSERT_TRUE(updatedFontSources[1]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
{
    return f->get_FullFontName() == u"Junction Light";
}))));

doc->Save(get_ArtifactsDir() + u"FontSettings.AddFontSource.pdf");

// Restaurez les sources de polices d'origine.
Aspose::Words::Fonts::FontSettings::get_DefaultInstance()->SetFontsSources(originalFontSources);
```

## Voir aussi

* Class [FontSourceBase](../../fontsourcebase/)
* Class [FontSettings](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
