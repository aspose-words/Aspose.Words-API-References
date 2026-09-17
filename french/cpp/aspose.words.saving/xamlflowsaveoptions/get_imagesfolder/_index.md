---
title: "Aspose::Words::Saving::XamlFlowSaveOptions::get_ImagesFolder méthode"
linktitle: "get_ImagesFolder"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Saving::XamlFlowSaveOptions::get_ImagesFolder méthode. Spécifie le dossier physique où les images sont enregistrées lors de l'exportation d'un document au format XAML. La valeur par défaut est une chaîne vide en C++."
type: docs
weight: 4000
url: /fr/cpp/aspose.words.saving/xamlflowsaveoptions/get_imagesfolder/
---
## XamlFlowSaveOptions::get_ImagesFolder method


Spécifie le dossier physique où les images sont enregistrées lors de l'exportation d'un document au format XAML. La valeur par défaut est une chaîne vide.

```cpp
System::String Aspose::Words::Saving::XamlFlowSaveOptions::get_ImagesFolder() const
```

## Remarques


Lorsque vous enregistrez un [Document](../../../aspose.words/document/) au format XAML, Aspose.Words doit enregistrer toutes les images incorporées dans le document en tant que fichiers autonomes. [ImagesFolder](./) vous permet de spécifier où les images seront enregistrées et [ImagesFolderAlias](../get_imagesfolderalias/) permet de spécifier comment les URI d'images seront construits.

Si vous enregistrez un document dans un fichier et fournissez un nom de fichier, Aspose.Words, par défaut, enregistre les images dans le même dossier où le fichier du document est enregistré. Utilisez [ImagesFolder](./) pour remplacer ce comportement.

Si vous enregistrez un document dans un flux, Aspose.Words n'a pas de dossier où enregistrer les images, mais doit tout de même les enregistrer quelque part. Dans ce cas, vous devez spécifier un dossier accessible dans la propriété [ImagesFolder](./) ou fournir des flux personnalisés via le gestionnaire d'événements [ImageSavingCallback](../get_imagesavingcallback/).

## Voir aussi

* Class [XamlFlowSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
