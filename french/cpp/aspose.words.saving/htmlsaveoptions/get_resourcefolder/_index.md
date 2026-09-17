---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_ResourceFolder méthode"
linktitle: "get_ResourceFolder"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_ResourceFolder méthode. Spécifie un dossier physique où toutes les ressources telles que les images, les polices et les CSS externes sont enregistrées lorsqu'un document est exporté en HTML. La valeur par défaut est une chaîne vide en C++."
type: docs
weight: 43000
url: /fr/cpp/aspose.words.saving/htmlsaveoptions/get_resourcefolder/
---
## HtmlSaveOptions::get_ResourceFolder method


Spécifie un dossier physique où toutes les ressources telles que les images, les polices et les CSS externes sont enregistrées lorsqu'un document est exporté vers HTML. La valeur par défaut est une chaîne vide.

```cpp
System::String Aspose::Words::Saving::HtmlSaveOptions::get_ResourceFolder() const
```

## Remarques


[ResourceFolder](./) is the simplest way to specify a folder where all resources should be written. Another way is to use individual properties [FontsFolder](../get_fontsfolder/), [ImagesFolder](../get_imagesfolder/), and [CssStyleSheetFileName](../get_cssstylesheetfilename/).

[ResourceFolder](./) has a lower priority than folders specified via [FontsFolder](../get_fontsfolder/), [ImagesFolder](../get_imagesfolder/), and [CssStyleSheetFileName](../get_cssstylesheetfilename/). For example, if both [ResourceFolder](./) and [FontsFolder](../get_fontsfolder/) are specified, fonts will be saved to [FontsFolder](../get_fontsfolder/), while images and CSS will be saved to [ResourceFolder](./).

Si le dossier spécifié par [ResourceFolder](./) n'existe pas, il sera créé automatiquement.

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
