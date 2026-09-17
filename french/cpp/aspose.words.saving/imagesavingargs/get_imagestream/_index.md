---
title: "Aspose::Words::Saving::ImageSavingArgs::get_ImageStream méthode"
linktitle: "get_ImageStream"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Saving::ImageSavingArgs::get_ImageStream méthode. Permet de spécifier le flux où l'image sera enregistrée en C++."
type: docs
weight: 5000
url: /fr/cpp/aspose.words.saving/imagesavingargs/get_imagestream/
---
## ImageSavingArgs::get_ImageStream method


Permet de spécifier le flux où l'image sera enregistrée.

```cpp
System::SharedPtr<System::IO::Stream> Aspose::Words::Saving::ImageSavingArgs::get_ImageStream() const
```

## Remarques


Cette propriété vous permet d’enregistrer des images dans des flux au lieu de fichiers lors du HTML.

La valeur par défaut est **null**. Lorsque cette propriété est **null**, l’image sera enregistrée dans un fichier spécifié dans la propriété [ImageFileName](../get_imagefilename/).

En utilisant [IImageSavingCallback](../../iimagesavingcallback/), vous ne pouvez pas remplacer une image par une autre. Il est destiné uniquement au contrôle de l’emplacement où enregistrer les images.

## Voir aussi

* Class [ImageSavingArgs](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
