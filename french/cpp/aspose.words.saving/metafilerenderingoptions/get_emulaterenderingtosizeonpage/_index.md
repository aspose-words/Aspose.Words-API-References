---
title: "Aspose::Words::Saving::MetafileRenderingOptions::get_EmulateRenderingToSizeOnPage méthode"
linktitle: "get_EmulateRenderingToSizeOnPage"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Saving::MetafileRenderingOptions::get_EmulateRenderingToSizeOnPage méthode. Obtient ou définit une valeur déterminant si le rendu du fichier métas émule l'affichage du fichier métas selon la taille sur la page ou l'affichage du fichier métas à sa taille par défaut en C++."
type: docs
weight: 4334
url: /fr/cpp/aspose.words.saving/metafilerenderingoptions/get_emulaterenderingtosizeonpage/
---
## MetafileRenderingOptions::get_EmulateRenderingToSizeOnPage method


Obtient ou définit une valeur déterminant si le rendu du métafichier émule l'affichage du métafichier selon la taille sur la page ou l'affichage du métafichier à sa taille par défaut.

```cpp
bool Aspose::Words::Saving::MetafileRenderingOptions::get_EmulateRenderingToSizeOnPage() const
```

## Remarques


Lorsque les fichiers métas sont affichés dans MS Word, certains graphiques peuvent être mis à l'échelle en fonction de la taille réelle du fichier métas en pixels. C’est‑à‑dire, même le zoom peut affecter l'affichage du fichier métas.

Lorsque cette valeur est définie sur **true**, Aspose.Words émule le rendu selon la taille du fichier métas sur la page. La taille en pixels est calculée à partir de la taille du fichier métas sur la page et de la [EmulateRenderingToSizeOnPageResolution](../get_emulaterenderingtosizeonpageresolution/) spécifiée.

Lorsque cette valeur est définie sur **false**, Aspose.Words émule le rendu du fichier métas à sa taille par défaut en pixels.

Cette option n'est utilisée que lorsque le fichier métas est rendu en graphiques vectoriels.

La valeur par défaut est **true**.
## Voir aussi

* Class [MetafileRenderingOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
