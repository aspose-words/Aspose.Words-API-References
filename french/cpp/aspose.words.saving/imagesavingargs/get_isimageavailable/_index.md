---
title: "Aspose::Words::Saving::ImageSavingArgs::get_IsImageAvailable méthode"
linktitle: "get_IsImageAvailable"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Saving::ImageSavingArgs::get_IsImageAvailable méthode. Retourne true si l'image actuelle est disponible pour l'exportation en C++."
type: docs
weight: 6000
url: /fr/cpp/aspose.words.saving/imagesavingargs/get_isimageavailable/
---
## ImageSavingArgs::get_IsImageAvailable method


Renvoie **true** si l'image actuelle est disponible pour l'exportation.

```cpp
bool Aspose::Words::Saving::ImageSavingArgs::get_IsImageAvailable() const
```

## Remarques


Certaines images du document peuvent être indisponibles, par exemple parce que l'image est liée et que le lien est inaccessible ou ne pointe pas vers une image valide. Dans ce cas, Aspose.Words exporte une icône avec une croix rouge. Cette propriété renvoie **true** si l'image originale est disponible ; renvoie **false** si l'image originale n'est pas disponible et une icône "no image" sera proposée pour l'enregistrement.

Lors de l'enregistrement d'un groupe de formes ou d'une forme qui ne nécessite aucune image, cette propriété est toujours **true**.

## Voir aussi

* Class [ImageSavingArgs](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
