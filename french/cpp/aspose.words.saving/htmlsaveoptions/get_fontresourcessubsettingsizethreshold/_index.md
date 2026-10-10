---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_FontResourcesSubsettingSizeThreshold méthode"
linktitle: "get_FontResourcesSubsettingSizeThreshold"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_FontResourcesSubsettingSizeThreshold méthode. Contrôle quelles ressources de police nécessitent un sous-ensemble lors de l'enregistrement au format HTML, MHTML ou EPUB. La valeur par défaut est %0 en C++."
type: docs
weight: 31000
url: /fr/cpp/aspose.words.saving/htmlsaveoptions/get_fontresourcessubsettingsizethreshold/
---
## HtmlSaveOptions::get_FontResourcesSubsettingSizeThreshold method


Contrôle quelles ressources de police nécessitent un sous‑ensemble lors de l’enregistrement en HTML, MHTML ou EPUB. La valeur par défaut est **%0**.

```cpp
int32_t Aspose::Words::Saving::HtmlSaveOptions::get_FontResourcesSubsettingSizeThreshold() const
```

## Remarques


[ExportFontResources](../get_exportfontresources/) allows exporting fonts as subsidiary files or as parts of the output package. If the document uses many fonts, especially with large number of glyphs, then output size can grow significantly. [Font](../../../aspose.words/font/) subsetting reduces the size of the exported font resource by filtering out glyphs that are not used by the current document.

[Font](../../../aspose.words/font/) subsetting works as follows:

* By default, all exported fonts are subsetted.
* Setting [FontResourcesSubsettingSizeThreshold](./) to a positive value instructs Aspose.Words to subset fonts which file size is larger than the specified value.
* Setting the property to **MaxValue** suppresses font subsetting.



**Important!** When exporting font resources, font licensing issues should be considered. Authors who want to use specific fonts via a downloadable font mechanism must always carefully verify that their intended use is within the scope of the font license. Many commercial fonts presently do not allow web downloading of their fonts in any form. [License](../../../aspose.words/license/) agreements that cover some fonts specifically note that usage via **%@font-face** rules in CSS style sheets is not allowed. [Font](../../../aspose.words/font/) subsetting can also violate license terms.

## Exemples



Montre comment travailler avec le sous-ensemble de polices.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Name(u"Arial");
builder->Writeln(u"Hello world!");
builder->get_Font()->set_Name(u"Times New Roman");
builder->Writeln(u"Hello world!");
builder->get_Font()->set_Name(u"Courier New");
builder->Writeln(u"Hello world!");

// Lorsque nous enregistrons le document au format HTML, nous pouvons passer un objet SaveOptions pour configurer le sous-ensemble de polices.
// Supposons que nous définissions le drapeau "ExportFontResources" sur "true" et que nous nommions également un dossier dans la propriété "FontsFolder".
// Dans ce cas, l'opération d'enregistrement créera ce dossier et y placera un fichier .ttf
// ce dossier pour chaque police que notre document utilise.
// Chaque fichier .ttf contiendra l'ensemble complet de glyphes de cette police,
// ce qui peut potentiellement entraîner un fichier très volumineux qui accompagne le document.
// Lorsque nous appliquons le sous-ensemble à une police, ses données brutes exportées ne contiendront que les glyphes que le document
// utilise au lieu de l'ensemble complet de glyphes. Si le texte de notre document n'utilise qu'une petite fraction du jeu de glyphes d'une police
// jeu de glyphes, alors le sous-ensemble réduira considérablement la taille de nos documents de sortie.
// Nous pouvons utiliser la propriété "FontResourcesSubsettingSizeThreshold" pour définir la taille d'un fichier .ttf, en octets.
// Si une police exportée crée un fichier de taille supérieure à cela, alors l'opération d'enregistrement appliquera le sous-ensemble à cette police.
// Définir un seuil de 0 applique le sous-ensemble à toutes les polices,
// et le définir à "int.MaxValue" désactive effectivement le sous-ensemble.
System::String fontsFolder = get_ArtifactsDir() + u"HtmlSaveOptions.FontSubsetting.Fonts";

auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
options->set_ExportFontResources(true);
options->set_FontsFolder(fontsFolder);
options->set_FontResourcesSubsettingSizeThreshold(fontResourcesSubsettingSizeThreshold);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.FontSubsetting.html", options);

System::ArrayPtr<System::String> fontFileNames = System::IO::Directory::GetFiles(fontsFolder)->LINQ_Where(static_cast<System::Func<System::String, bool>>(static_cast<std::function<bool(System::String s)>>([](System::String s) -> bool
{
    return s.EndsWith(u".ttf");
})))->LINQ_ToArray();

ASSERT_EQ(3, fontFileNames->get_Length());

for (System::String filename : fontFileNames)
{
    // Par défaut, les fichiers .ttf de chacune de nos trois polices dépasseront 700 Mo.
    // Le sous-ensemble les réduira tous à moins de 30 Mo.
    auto fontFileInfo = System::MakeObject<System::IO::FileInfo>(filename);

    ASSERT_TRUE(fontFileInfo->get_Length() > 700000 || fontFileInfo->get_Length() < 30000);
    ASSERT_TRUE(System::Math::Max(fontResourcesSubsettingSizeThreshold, 30000) > System::MakeObject<System::IO::FileInfo>(filename)->get_Length());
}
```

## Voir aussi

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
