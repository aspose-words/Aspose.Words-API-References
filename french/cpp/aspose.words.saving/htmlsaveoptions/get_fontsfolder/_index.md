---
title: "Méthode Aspose::Words::Saving::HtmlSaveOptions::get_FontsFolder"
linktitle: "get_FontsFolder"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Saving::HtmlSaveOptions::get_FontsFolder. Spécifie le dossier physique où les polices sont enregistrées lors de l'exportation d'un document vers HTML. La valeur par défaut est une chaîne vide en C++."
type: docs
weight: 33000
url: /fr/cpp/aspose.words.saving/htmlsaveoptions/get_fontsfolder/
---
## HtmlSaveOptions::get_FontsFolder method


Spécifie le dossier physique où les polices sont enregistrées lors de l’exportation d’un document en HTML. La valeur par défaut est une chaîne vide.

```cpp
System::String Aspose::Words::Saving::HtmlSaveOptions::get_FontsFolder() const
```

## Remarques


Lorsque vous enregistrez un [Document](../../../aspose.words/document/) au format HTML et que [ExportFontResources](../get_exportfontresources/) est défini sur **true**, Aspose.Words doit enregistrer les polices utilisées dans le document en tant que fichiers autonomes. [FontsFolder](./) vous permet de spécifier où les polices seront enregistrées et [FontsFolderAlias](../get_fontsfolderalias/) permet de spécifier comment les URI de police seront construits.

Si vous enregistrez un document dans un fichier et fournissez un nom de fichier, Aspose.Words, par défaut, enregistre les polices dans le même dossier où le fichier du document est enregistré. Utilisez [FontsFolder](./) pour remplacer ce comportement.

Si vous enregistrez un document dans un flux, Aspose.Words n'a pas de dossier où enregistrer les polices, mais doit tout de même les enregistrer quelque part. Dans ce cas, vous devez spécifier un dossier accessible dans la propriété [FontsFolder](./) ou fournir des flux personnalisés via le gestionnaire d'événement [FontSavingCallback](../get_fontsavingcallback/).

Si le dossier spécifié par [FontsFolder](./) n'existe pas, il sera créé automatiquement.

[ResourceFolder](../get_resourcefolder/) is another way to specify a folder where fonts should be saved.

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
