---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_ResourceFolderAlias method"
linktitle: "get_ResourceFolderAlias"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_ResourceFolderAlias method. Spécifie le nom du dossier utilisé pour construire les URI de toutes les ressources écrites dans un document HTML. La valeur par défaut est une chaîne vide en C++."
type: docs
weight: 44000
url: /fr/cpp/aspose.words.saving/htmlsaveoptions/get_resourcefolderalias/
---
## HtmlSaveOptions::get_ResourceFolderAlias method


Spécifie le nom du dossier utilisé pour construire les URI de toutes les ressources écrites dans un document HTML. La valeur par défaut est une chaîne vide.

```cpp
System::String Aspose::Words::Saving::HtmlSaveOptions::get_ResourceFolderAlias() const
```

## Remarques


[ResourceFolderAlias](./) is the simplest way to specify how URIs for all resource files should be constructed. Same information can be specified for images and fonts separately via [ImagesFolderAlias](../get_imagesfolderalias/) and [FontsFolderAlias](../get_fontsfolderalias/) properties, respectively. However, there is no individual property for CSS.

[ResourceFolderAlias](./) has lower priority than [FontsFolderAlias](../get_fontsfolderalias/) and [ImagesFolderAlias](../get_imagesfolderalias/). For example, if both [ResourceFolderAlias](./) and [FontsFolderAlias](../get_fontsfolderalias/) are specified, fonts' URIs will be constructed using [FontsFolderAlias](../get_fontsfolderalias/), while URIs of images and CSS will be constructed using [ResourceFolderAlias](./).

Si [ResourceFolderAlias](./) est vide, la valeur de la propriété [ResourceFolder](../get_resourcefolder/) sera utilisée pour construire les URI des ressources.

Si [ResourceFolderAlias](./) est défini sur '.' (point), les URI des ressources ne contiendront que les noms de fichiers, sans aucun chemin.

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
