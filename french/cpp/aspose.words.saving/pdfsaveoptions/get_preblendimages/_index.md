---
title: "Méthode Aspose::Words::Saving::PdfSaveOptions::get_PreblendImages"
linktitle: "get_PreblendImages"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Saving::PdfSaveOptions::get_PreblendImages. Obtient ou définit une valeur déterminant s’il faut ou non pré‑mélanger les images transparentes avec une couleur d’arrière‑plan noire en C++."
type: docs
weight: 27000
url: /fr/cpp/aspose.words.saving/pdfsaveoptions/get_preblendimages/
---
## PdfSaveOptions::get_PreblendImages method


Obtient ou définit une valeur déterminant s'il faut ou non pré-mélanger les images transparentes avec une couleur d'arrière-plan noire.

```cpp
bool Aspose::Words::Saving::PdfSaveOptions::get_PreblendImages() const
```

## Remarques


Le pré‑mélange des images peut améliorer l’apparence visuelle du document PDF dans Adobe Reader et supprimer les artefacts d’anti‑aliasing.

Afin d’afficher correctement les images pré‑mélangées, l’application de visualisation PDF doit prendre en charge l’entrée /Matte dans le dictionnaire d’image à masque souple. De plus, le pré‑mélange des images peut réduire les performances de rendu du PDF.

La valeur par défaut est **false**.
## Voir aussi

* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
