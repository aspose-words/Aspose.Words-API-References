---
title: "Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportEmbeddedFonts méthode"
linktitle: "get_ExportEmbeddedFonts"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportEmbeddedFonts méthode. Spécifie si les polices doivent être intégrées dans le document Html au format Base64. Notez que la définition de ce drapeau peut augmenter de façon significative la taille du fichier Html de sortie en C++."
type: docs
weight: 6000
url: /fr/cpp/aspose.words.saving/htmlfixedsaveoptions/get_exportembeddedfonts/
---
## HtmlFixedSaveOptions::get_ExportEmbeddedFonts method


Spécifie si les polices doivent être incorporées dans le document Html au format Base64. Notez que l'activation de ce drapeau peut augmenter considérablement la taille du fichier Html de sortie.

```cpp
bool Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportEmbeddedFonts() const
```


## Exemples



Montre comment déterminer où stocker les polices intégrées lors de l'exportation d'un document vers Html.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Embedded font.docx");

// Lorsque nous exportons un document avec des polices intégrées vers .html,
// Aspose.Words peut placer les polices dans deux emplacements possibles.
// Définir le drapeau "ExportEmbeddedFonts" sur "true" stockera les données brutes des polices intégrées dans la feuille de style CSS,
// dans la propriété "url" de la règle "@font-face". Cela peut créer un fichier de feuille de style CSS énorme
// et réduire le nombre de fichiers externes que cette conversion HTML créera.
// Définir ce drapeau sur "false" créera un fichier pour chaque police.
// La feuille de style CSS liera chaque fichier de police en utilisant la propriété "url" de la règle "@font-face".
auto htmlFixedSaveOptions = System::MakeObject<Aspose::Words::Saving::HtmlFixedSaveOptions>();
htmlFixedSaveOptions->set_ExportEmbeddedFonts(exportEmbeddedFonts);

doc->Save(get_ArtifactsDir() + u"HtmlFixedSaveOptions.ExportEmbeddedFonts.html", htmlFixedSaveOptions);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlFixedSaveOptions.ExportEmbeddedFonts/styles.css");

if (exportEmbeddedFonts)
{
    ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(outDocContents, u"@font-face { font-family:'Arial'; font-style:normal; font-weight:normal; src:local[(]'☺'[)], url[(].+[)] format[(]'woff'[)]; }")->get_Success());
    ASSERT_EQ(0, System::IO::Directory::GetFiles(get_ArtifactsDir() + u"HtmlFixedSaveOptions.ExportEmbeddedFonts")->LINQ_Count(static_cast<System::Func<System::String, bool>>(static_cast<std::function<bool(System::String f)>>([](System::String f) -> bool
    {
        return f.EndsWith(u".woff");
    }))));
}
else
{
    ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(outDocContents, u"@font-face { font-family:'Arial'; font-style:normal; font-weight:normal; src:local[(]'☺'[)], url[(]'font001[.]woff'[)] format[(]'woff'[)]; }")->get_Success());
    ASSERT_EQ(2, System::IO::Directory::GetFiles(get_ArtifactsDir() + u"HtmlFixedSaveOptions.ExportEmbeddedFonts")->LINQ_Count(static_cast<System::Func<System::String, bool>>(static_cast<std::function<bool(System::String f)>>([](System::String f) -> bool
    {
        return f.EndsWith(u".woff");
    }))));
}
```

## Voir aussi

* Class [HtmlFixedSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
