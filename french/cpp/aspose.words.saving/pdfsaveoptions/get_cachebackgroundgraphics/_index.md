---
title: "Aspose::Words::Saving::PdfSaveOptions::get_CacheBackgroundGraphics méthode"
linktitle: "get_CacheBackgroundGraphics"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Saving::PdfSaveOptions::get_CacheBackgroundGraphics méthode. Obtient ou définit une valeur déterminant s'il faut mettre en cache ou non les graphiques placés dans l'arrière-plan du document en C++."
type: docs
weight: 5000
url: /fr/cpp/aspose.words.saving/pdfsaveoptions/get_cachebackgroundgraphics/
---
## PdfSaveOptions::get_CacheBackgroundGraphics method


Obtient ou définit une valeur déterminant s'il faut mettre en cache ou non les graphiques placés en arrière-plan du document.

```cpp
bool Aspose::Words::Saving::PdfSaveOptions::get_CacheBackgroundGraphics() const
```

## Remarques


La valeur par défaut est **true** et les graphiques d'arrière-plan sont écrits dans le document PDF sous forme d'un xObject.

Lorsque la valeur est **false**, les graphiques d'arrière-plan ne sont pas mis en cache.

Certaines formes ne sont pas prises en charge pour la mise en cache (formes avec champs, signets, HRefs).

[Document](../../../aspose.words/document/) background graphic is various shapes, charts, images placed in the footer or header, well as background and border of a page. 
## Voir aussi

* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
