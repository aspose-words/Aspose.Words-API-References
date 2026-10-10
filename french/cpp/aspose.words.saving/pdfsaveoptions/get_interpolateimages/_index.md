---
title: "Méthode Aspose::Words::Saving::PdfSaveOptions::get_InterpolateImages"
linktitle: "get_InterpolateImages"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Saving::PdfSaveOptions::get_InterpolateImages. Un indicateur indiquant si l'interpolation d'image doit être effectuée par un lecteur conforme. Lorsque **false** est spécifié, l'indicateur n'est pas écrit dans le document de sortie et le comportement par défaut du lecteur est utilisé à la place dans C++."
type: docs
weight: 22000
url: /fr/cpp/aspose.words.saving/pdfsaveoptions/get_interpolateimages/
---
## PdfSaveOptions::get_InterpolateImages method


Un indicateur indiquant si l'interpolation d'image doit être effectuée par un lecteur conforme. Lorsque **false** est spécifié, l'indicateur n'est pas écrit dans le document de sortie et le comportement par défaut du lecteur est utilisé à la place.

```cpp
bool Aspose::Words::Saving::PdfSaveOptions::get_InterpolateImages() const
```

## Remarques


Lorsque la résolution d'une image source est nettement inférieure à celle du dispositif de sortie, chaque échantillon source couvre de nombreux pixels du dispositif. En conséquence, les images peuvent apparaître en escalier ou pixélisées. Ces artefacts visuels peuvent être réduits en appliquant un algorithme d'interpolation d'image lors du rendu. Au lieu de peindre tous les pixels couverts par un échantillon source avec la même couleur, l'interpolation d'image tente de produire une transition fluide entre les valeurs d'échantillons adjacentes.

Un lecteur conforme peut choisir de ne pas implémenter cette fonctionnalité du PDF, ou peut utiliser toute implémentation spécifique d'interpolation qu'il souhaite.

La valeur par défaut est **false**.

Le drapeau d'interpolation est interdit par la conformité PDF/A. La valeur **false** sera utilisée automatiquement lors de l'enregistrement en PDF/A.
## Voir aussi

* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
