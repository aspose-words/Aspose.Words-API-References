---
title: "Aspose::Words::Saving::MetafileRenderingOptions::get_EmfPlusDualRenderingMode méthode"
linktitle: "get_EmfPlusDualRenderingMode"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Saving::MetafileRenderingOptions::get_EmfPlusDualRenderingMode méthode. Obtient ou définit une valeur déterminant comment les métafichiers EMF+ Dual doivent être rendus en C++."
type: docs
weight: 3000
url: /fr/cpp/aspose.words.saving/metafilerenderingoptions/get_emfplusdualrenderingmode/
---
## MetafileRenderingOptions::get_EmfPlusDualRenderingMode method


Obtient ou définit une valeur déterminant comment les métafichiers EMF+ Dual doivent être rendus.

```cpp
Aspose::Words::Saving::EmfPlusDualRenderingMode Aspose::Words::Saving::MetafileRenderingOptions::get_EmfPlusDualRenderingMode() const
```

## Remarques


Les métafichiers EMF+ Dual contiennent à la fois des parties EMF+ et EMF. MS Word et GDI+ rendent toujours la partie EMF+. Aspose.Words ne prend actuellement pas entièrement en charge tous les enregistrements EMF+ et, dans certains cas, le rendu de la partie EMF semble meilleur que celui de la partie EMF+.

Cette option n’est utilisée que lorsque le métafichier est rendu sous forme de graphiques vectoriels. Lorsque le métafichier est rendu en bitmap, la partie EMF+ est toujours utilisée.

La valeur par défaut est [EmfPlusWithFallback](../../emfplusdualrenderingmode/).
## Voir aussi

* Enum [EmfPlusDualRenderingMode](../../emfplusdualrenderingmode/)
* Class [MetafileRenderingOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
