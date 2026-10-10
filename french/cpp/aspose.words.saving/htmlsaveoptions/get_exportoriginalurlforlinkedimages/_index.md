---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportOriginalUrlForLinkedImages méthode"
linktitle: "get_ExportOriginalUrlForLinkedImages"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportOriginalUrlForLinkedImages méthode. Spécifie si l'URL originale doit être utilisée comme URL des images liées. La valeur par défaut est false en C++."
type: docs
weight: 22000
url: /fr/cpp/aspose.words.saving/htmlsaveoptions/get_exportoriginalurlforlinkedimages/
---
## HtmlSaveOptions::get_ExportOriginalUrlForLinkedImages method


Spécifie si l'URL d'origine doit être utilisée comme URL des images liées. La valeur par défaut est **false**.

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ExportOriginalUrlForLinkedImages() const
```

## Remarques


Si la valeur est définie sur **true**[SourceFullName](../../../aspose.words.drawing/imagedata/get_sourcefullname/) la valeur est utilisée comme URL des images liées et les images liées ne sont pas chargées dans le dossier du document ou [ImagesFolder](../get_imagesfolder/).

Si la valeur est définie sur **false** les images liées sont chargées dans le dossier du document ou [ImagesFolder](../get_imagesfolder/) et l'URL de chaque image liée est construite en fonction du dossier du document, [ImagesFolder](../get_imagesfolder/) et des propriétés [ImagesFolderAlias](../get_imagesfolderalias/).

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
