---
title: "Méthode Aspose::Words::Saving::HtmlSaveOptions::get_FontsFolderAlias"
linktitle: "get_FontsFolderAlias"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Saving::HtmlSaveOptions::get_FontsFolderAlias. Spécifie le nom du dossier utilisé pour construire les URI de police écrites dans un document HTML. La valeur par défaut est une chaîne vide en C++."
type: docs
weight: 34000
url: /fr/cpp/aspose.words.saving/htmlsaveoptions/get_fontsfolderalias/
---
## HtmlSaveOptions::get_FontsFolderAlias method


Spécifie le nom du dossier utilisé pour construire les URI de police écrites dans un document HTML. La valeur par défaut est une chaîne vide.

```cpp
System::String Aspose::Words::Saving::HtmlSaveOptions::get_FontsFolderAlias() const
```

## Remarques


Lorsque vous enregistrez un [Document](../../../aspose.words/document/) au format HTML et que [ExportFontResources](../get_exportfontresources/) est défini sur **true**, Aspose.Words doit enregistrer les polices utilisées dans le document en tant que fichiers autonomes. [FontsFolder](../get_fontsfolder/) vous permet de spécifier où les polices seront enregistrées et [FontsFolderAlias](./) permet de spécifier comment les URI de police seront construits.

Si [FontsFolderAlias](./) n'est pas une chaîne vide, alors l'URI de police écrite dans le HTML sera *FontsFolderAlias + <font file name>*.

Si [FontsFolderAlias](./) est une chaîne vide, alors l'URI de police écrite dans le HTML sera *FontsFolder + <font file name>*.

Si [FontsFolderAlias](./) est défini sur '.' (point), alors le nom du fichier de police sera écrit dans le HTML sans chemin, quel que soit les autres options.

Une façon alternative de spécifier le nom du dossier pour construire les URI de police consiste à utiliser [ResourceFolderAlias](../get_resourcefolderalias/).

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
