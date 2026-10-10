---
title: "Aspose::Words::Saving::MetafileRenderingMode enum"
linktitle: "MetafileRenderingMode"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Saving::MetafileRenderingMode enum. Spécifie comment Aspose.Words doit rendre les métafichiers WMF et EMF en C++."
type: docs
weight: 69000
url: /fr/cpp/aspose.words.saving/metafilerenderingmode/
---
## MetafileRenderingMode enum


Spécifie comment Aspose.Words doit rendre les métafichiers WMF et EMF.

```cpp
enum class MetafileRenderingMode
```

### Valeurs

| Nom | Valeur | Description |
| --- | --- | --- |
| VectorWithFallback | 0 | Aspose.Words tente de rendre un métafile sous forme de graphiques vectoriels. Si Aspose.Words ne peut pas rendre correctement certains enregistrements du métafile en graphiques vectoriels, alors Aspose.Words rend ce métafile en bitmap. |
| Vector | 1 | Aspose.Words rend un métafichier en tant que graphiques vectoriels. |
| Bitmap | 2 | Aspose.Words invoque GDI+ pour rendre un métafichier en bitmap, puis enregistre le bitmap dans le document de sortie. |

## Voir aussi

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
