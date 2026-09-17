---
title: "Aspose::Words::Saving::MarkdownSaveOptions::get_ImagesFolderAlias method"
linktitle: "get_ImagesFolderAlias"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Saving::MarkdownSaveOptions::get_ImagesFolderAlias method. Spécifie le nom du dossier utilisé pour construire les URI d'images écrites dans un document. La valeur par défaut est une chaîne vide en C++."
type: docs
weight: 5500
url: /fr/cpp/aspose.words.saving/markdownsaveoptions/get_imagesfolderalias/
---
## MarkdownSaveOptions::get_ImagesFolderAlias method


Spécifie le nom du dossier utilisé pour construire les URI d'images écrites dans un document. La valeur par défaut est une chaîne vide.

```cpp
System::String Aspose::Words::Saving::MarkdownSaveOptions::get_ImagesFolderAlias() const
```

## Remarques


Lorsque vous enregistrez un [Document](../../../aspose.words/document/) au format [Markdown](../../../aspose.words/saveformat/), Aspose.Words doit enregistrer toutes les images incorporées dans le document en tant que fichiers autonomes. [ImagesFolder](../get_imagesfolder/) vous permet de spécifier où les images seront enregistrées et [ImagesFolderAlias](./) permet de spécifier comment les URI d'images seront construites.

Si [ImagesFolderAlias](./) n'est pas une chaîne vide, alors l'URI d'image écrit dans le Markdown sera *ImagesFolderAlias + <image file name>*.

Si [ImagesFolderAlias](./) est une chaîne vide, alors l'URI d'image écrit dans le Markdown sera *ImagesFolder + <image file name>*.

Si [ImagesFolderAlias](./) est défini sur '.' (point), alors le nom du fichier image sera écrit dans le Markdown sans chemin, quel que soit les autres options.

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
