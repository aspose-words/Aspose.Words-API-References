---
title: "Aspose::Words::Saving::MetafileRenderingOptions::get_EmulateRasterOperations méthode"
linktitle: "get_EmulateRasterOperations"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Saving::MetafileRenderingOptions::get_EmulateRasterOperations méthode. Obtient ou définit une valeur déterminant si les opérations raster doivent être émulées en C++."
type: docs
weight: 4000
url: /fr/cpp/aspose.words.saving/metafilerenderingoptions/get_emulaterasteroperations/
---
## MetafileRenderingOptions::get_EmulateRasterOperations method


Obtient ou définit une valeur déterminant si les opérations raster doivent être émulées.

```cpp
bool Aspose::Words::Saving::MetafileRenderingOptions::get_EmulateRasterOperations() const
```

## Remarques


Des opérations raster spécifiques peuvent être utilisées dans les fichiers métas. Elles ne peuvent pas être rendues directement en graphiques vectoriels. L'émulation des opérations raster nécessite une rasterisation partielle des graphiques vectoriels résultants, ce qui peut affecter les performances du rendu du fichier métas.

Lorsque cette valeur est définie sur **true**, Aspose.Words émule les opérations raster. La sortie résultante peut être partiellement rasterisée et les performances peuvent être plus lentes.

Lorsque cette valeur est définie sur **false**, Aspose.Words n'émule pas les opérations raster. Lorsque [Aspose.Words](../../../aspose.words/) rencontre une opération raster dans un fichier métas, il revient au rendu du fichier métas en bitmap en utilisant le système d'exploitation.

Cette option n'est utilisée que lorsque le fichier métas est rendu en graphiques vectoriels.

La valeur par défaut est **true**.
## Voir aussi

* Class [MetafileRenderingOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
