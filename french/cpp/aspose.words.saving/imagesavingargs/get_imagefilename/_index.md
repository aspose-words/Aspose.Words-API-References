---
title: "Aspose::Words::Saving::ImageSavingArgs::get_ImageFileName méthode"
linktitle: "get_ImageFileName"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Saving::ImageSavingArgs::get_ImageFileName méthode. Obtient ou définit le nom de fichier (sans le chemin) où l'image sera enregistrée en C++."
type: docs
weight: 4000
url: /fr/cpp/aspose.words.saving/imagesavingargs/get_imagefilename/
---
## ImageSavingArgs::get_ImageFileName method


Obtient ou définit le nom de fichier (sans le chemin) où l'image sera enregistrée.

```cpp
System::String Aspose::Words::Saving::ImageSavingArgs::get_ImageFileName() const
```

## Remarques


Cette propriété vous permet de redéfinir la façon dont les noms de fichiers d'image sont générés lors de l'exportation vers HTML.

Lorsque l'événement est déclenché, cette propriété contient le nom de fichier généré par Aspose.Words. Vous pouvez modifier la valeur de cette propriété pour enregistrer l'image dans un fichier différent. Notez que les noms de fichiers doivent être uniques.

Aspose.Words génère automatiquement un nom de fichier unique pour chaque image incorporée lors de l'exportation au format HTML. La façon dont le nom de fichier de l'image est généré dépend de si vous enregistrez le document dans un fichier ou dans un flux.

Lors de l'enregistrement d'un document dans un fichier, le nom de fichier d'image généré ressemble à *%<document base file name>.<image number>.<extension>*.

Lors de l'enregistrement d'un document dans un flux, le nom de fichier d'image généré ressemble à *Aspose.Words.<document guid>.<image number>.<extension>*.

[ImageFileName](./) must contain only the file name without the path. Aspose.Words determines the path for saving and the value of the **src** attribute for writing to HTML using the document file name, the [ImagesFolder](../../htmlsaveoptions/get_imagesfolder/) and [ImagesFolderAlias](../../htmlsaveoptions/get_imagesfolderalias/) properties.

## Voir aussi

* Class [ImageSavingArgs](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
