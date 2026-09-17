---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_ImagesFolderAlias méthode"
linktitle: "get_ImagesFolderAlias"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_ImagesFolderAlias méthode. Spécifie le nom du dossier utilisé pour construire les URI d'images écrits dans un document HTML. La valeur par défaut est une chaîne vide en C++."
type: docs
weight: 39000
url: /fr/cpp/aspose.words.saving/htmlsaveoptions/get_imagesfolderalias/
---
## HtmlSaveOptions::get_ImagesFolderAlias method


Spécifie le nom du dossier utilisé pour construire les URI d’image écrites dans un document HTML. La valeur par défaut est une chaîne vide.

```cpp
System::String Aspose::Words::Saving::HtmlSaveOptions::get_ImagesFolderAlias() const
```

## Remarques


Lorsque vous enregistrez un [Document](../../../aspose.words/document/) au format HTML, Aspose.Words doit enregistrer toutes les images incorporées dans le document en tant que fichiers autonomes. [ImagesFolder](../get_imagesfolder/) vous permet de spécifier où les images seront enregistrées et [ImagesFolderAlias](./) permet de spécifier comment les URI d'images seront construits.

Si [ImagesFolderAlias](./) n'est pas une chaîne vide, alors l'URI d'image écrit dans le HTML sera *ImagesFolderAlias + <image file name>*.

Si [ImagesFolderAlias](./) est une chaîne vide, alors l'URI d'image écrit dans le HTML sera *ImagesFolder + <image file name>*.

Si [ImagesFolderAlias](./) est défini sur '.' (point), alors le nom du fichier image sera écrit dans le HTML sans chemin, quel que soit les autres options.

Une façon alternative de spécifier le nom du dossier pour construire les URI d'images consiste à utiliser [ResourceFolderAlias](../get_resourcefolderalias/).

## Exemples



Montre comment définir des dossiers et des alias de dossiers pour les ressources enregistrées à l'extérieur que Aspose.Words créera lors de l'enregistrement d'un document en HTML.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
options->set_CssStyleSheetType(Aspose::Words::Saving::CssStyleSheetType::External);
options->set_ExportFontResources(true);
options->set_ImageResolution(72);
options->set_FontResourcesSubsettingSizeThreshold(0);
options->set_FontsFolder(get_ArtifactsDir() + u"Fonts");
options->set_ImagesFolder(get_ArtifactsDir() + u"Images");
options->set_ResourceFolder(get_ArtifactsDir() + u"Resources");
options->set_FontsFolderAlias(u"http://example.com/fonts");
options->set_ImagesFolderAlias(u"http://example.com/images");
options->set_ResourceFolderAlias(u"http://example.com/resources");
options->set_ExportOriginalUrlForLinkedImages(true);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.FolderAlias.html", options);
```

## Voir aussi

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
