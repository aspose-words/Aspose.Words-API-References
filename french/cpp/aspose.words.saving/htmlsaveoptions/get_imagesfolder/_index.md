---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_ImagesFolder méthode"
linktitle: "get_ImagesFolder"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_ImagesFolder méthode. Spécifie le dossier physique où les images sont enregistrées lors de l'exportation d'un document au format HTML. La valeur par défaut est une chaîne vide en C++."
type: docs
weight: 38000
url: /fr/cpp/aspose.words.saving/htmlsaveoptions/get_imagesfolder/
---
## HtmlSaveOptions::get_ImagesFolder method


Spécifie le dossier physique où les images sont enregistrées lors de l’exportation d’un document au format HTML. La valeur par défaut est une chaîne vide.

```cpp
System::String Aspose::Words::Saving::HtmlSaveOptions::get_ImagesFolder() const
```

## Remarques


Lorsque vous enregistrez un [Document](../../../aspose.words/document/) au format HTML, Aspose.Words doit enregistrer toutes les images incorporées dans le document en tant que fichiers autonomes. [ImagesFolder](./) vous permet de spécifier où les images seront enregistrées et [ImagesFolderAlias](../get_imagesfolderalias/) permet de spécifier comment les URI des images seront construites.

Si vous enregistrez un document dans un fichier et fournissez un nom de fichier, Aspose.Words, par défaut, enregistre les images dans le même dossier où le fichier du document est enregistré. Utilisez [ImagesFolder](./) pour remplacer ce comportement.

Si vous enregistrez un document dans un flux, Aspose.Words n'a pas de dossier où enregistrer les images, mais doit tout de même les enregistrer quelque part. Dans ce cas, vous devez spécifier un dossier accessible dans la propriété [ImagesFolder](./) ou fournir des flux personnalisés via le gestionnaire d'événements [ImageSavingCallback](../get_imagesavingcallback/).

Si le dossier spécifié par [ImagesFolder](./) n'existe pas, il sera créé automatiquement.

[ResourceFolder](../get_resourcefolder/) is another way to specify a folder where images should be saved.

## Exemples



Montre comment spécifier le dossier pour stocker les images liées après l'enregistrement au format .html.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

System::String imagesDir = System::IO::Path::Combine(get_ArtifactsDir(), u"SaveHtmlWithOptions");

if (System::IO::Directory::Exists(imagesDir))
{
    System::IO::Directory::Delete(imagesDir, true);
}

System::IO::Directory::CreateDirectory_(imagesDir);

// Définissez une option pour exporter les champs de formulaire en texte brut au lieu d'éléments d'entrée HTML.
auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>(Aspose::Words::SaveFormat::Html);
options->set_ExportTextInputFormFieldAsText(true);
options->set_ImagesFolder(imagesDir);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.SaveHtmlWithOptions.html", options);
```

## Voir aussi

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
