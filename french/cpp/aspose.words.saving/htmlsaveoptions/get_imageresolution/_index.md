---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_ImageResolution méthode"
linktitle: "get_ImageResolution"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_ImageResolution méthode. Spécifie la résolution de sortie pour les images lors de l'exportation vers HTML, MHTML ou EPUB. La valeur par défaut est %96 dpi en C++."
type: docs
weight: 36000
url: /fr/cpp/aspose.words.saving/htmlsaveoptions/get_imageresolution/
---
## HtmlSaveOptions::get_ImageResolution method


Spécifie la résolution de sortie pour les images lors de l’exportation en HTML, MHTML ou EPUB. La valeur par défaut est **%96 dpi**.

```cpp
int32_t Aspose::Words::Saving::HtmlSaveOptions::get_ImageResolution() const
```

## Remarques


Cette propriété affecte les images matricielles lorsque [ScaleImageToShapeSize](../get_scaleimagetoshapesize/) est **true** et affecte les métafichiers exportés en tant qu'images matricielles. Certaines propriétés d'image telles que le recadrage ou la rotation nécessitent d'enregistrer des images transformées et, dans ce cas, les images transformées sont créées à la résolution donnée.

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
