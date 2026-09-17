---
title: "Aspose::Words::Saving::MarkdownSaveOptions::get_ImagesFolder méthode"
linktitle: "get_ImagesFolder"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Saving::MarkdownSaveOptions::get_ImagesFolder méthode. Spécifie le dossier physique où les images sont enregistrées lors de l'exportation d'un document au format Markdown. La valeur par défaut est une chaîne vide en C++."
type: docs
weight: 5000
url: /fr/cpp/aspose.words.saving/markdownsaveoptions/get_imagesfolder/
---
## MarkdownSaveOptions::get_ImagesFolder method


Spécifie le dossier physique où les images sont enregistrées lors de l'exportation d'un document au format [Markdown](../../../aspose.words/saveformat/). La valeur par défaut est une chaîne vide.

```cpp
System::String Aspose::Words::Saving::MarkdownSaveOptions::get_ImagesFolder() const
```

## Remarques


Lorsque vous enregistrez un [Document](../../../aspose.words/document/) au format [Markdown](../../../aspose.words/saveformat/), Aspose.Words doit enregistrer toutes les images incorporées dans le document en tant que fichiers autonomes. [ImagesFolder](./) vous permet de spécifier où les images seront enregistrées.

Si vous enregistrez un document dans un fichier et fournissez un nom de fichier, Aspose.Words, par défaut, enregistre les images dans le même dossier où le fichier du document est enregistré. Utilisez [ImagesFolder](./) pour remplacer ce comportement.

Si vous enregistrez un document dans un flux, Aspose.Words n'a pas de dossier où enregistrer les images, mais doit tout de même les enregistrer quelque part. Dans ce cas, vous devez spécifier un dossier accessible dans la propriété [ImagesFolder](./).

Si le dossier spécifié par [ImagesFolder](./) n'existe pas, il sera créé automatiquement.

## Exemples



Montre comment spécifier le nom du dossier utilisé pour construire les URI d'images.
```cpp
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>();

builder->Writeln(u"Some image below:");
builder->InsertImage(get_ImageDir() + u"Logo.jpg");

System::String imagesFolder = System::IO::Path::Combine(get_ArtifactsDir(), u"ImagesDir");
auto saveOptions = System::MakeObject<Aspose::Words::Saving::MarkdownSaveOptions>();
// Utilisez la propriété "ImagesFolder" pour assigner un dossier du système de fichiers local dans lequel
// Aspose.Words enregistrera toutes les images liées du document.
saveOptions->set_ImagesFolder(imagesFolder);
// Utilisez la propriété "ImagesFolderAlias" pour utiliser ce dossier
// lors de la construction des URI d'images au lieu du nom du dossier d'images.
saveOptions->set_ImagesFolderAlias(u"http://example.com/images");

builder->get_Document()->Save(get_ArtifactsDir() + u"MarkdownSaveOptions.ImagesFolder.md", saveOptions);
```

## Voir aussi

* Class [MarkdownSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
