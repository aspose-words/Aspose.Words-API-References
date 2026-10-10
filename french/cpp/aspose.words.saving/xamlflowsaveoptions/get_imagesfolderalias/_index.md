---
title: "Aspose::Words::Saving::XamlFlowSaveOptions::get_ImagesFolderAlias méthode"
linktitle: "get_ImagesFolderAlias"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Saving::XamlFlowSaveOptions::get_ImagesFolderAlias méthode. Spécifie le nom du dossier utilisé pour construire les URI d'images écrites dans un document XAML. La valeur par défaut est une chaîne vide en C++."
type: docs
weight: 5000
url: /fr/cpp/aspose.words.saving/xamlflowsaveoptions/get_imagesfolderalias/
---
## XamlFlowSaveOptions::get_ImagesFolderAlias method


Spécifie le nom du dossier utilisé pour construire les URI d'images écrites dans un document XAML. La valeur par défaut est une chaîne vide.

```cpp
System::String Aspose::Words::Saving::XamlFlowSaveOptions::get_ImagesFolderAlias() const
```

## Remarques


Lorsque vous enregistrez un [Document](../../../aspose.words/document/) au format XAML, Aspose.Words doit enregistrer toutes les images incorporées dans le document en tant que fichiers autonomes. [ImagesFolder](../get_imagesfolder/) vous permet de spécifier où les images seront enregistrées et [ImagesFolderAlias](./) permet de spécifier comment les URI d'images seront construits.

Si [ImagesFolderAlias](./) n'est pas une chaîne vide, alors l'URI d'image écrite dans le XAML sera *ImagesFolderAlias + <image file name>*.

Si [ImagesFolderAlias](./) est une chaîne vide, alors l'URI d'image écrite dans le XAML sera *ImagesFolder + <image file name>*.

Si [ImagesFolderAlias](./) est défini sur '.' (point), alors le nom du fichier image sera écrit dans le XAML sans chemin, quel que soit les autres options.

## Voir aussi

* Class [XamlFlowSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
