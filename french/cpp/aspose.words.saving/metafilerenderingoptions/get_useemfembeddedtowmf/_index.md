---
title: "Aspose::Words::Saving::MetafileRenderingOptions::get_UseEmfEmbeddedToWmf méthode"
linktitle: "get_UseEmfEmbeddedToWmf"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Saving::MetafileRenderingOptions::get_UseEmfEmbeddedToWmf méthode. Obtient ou définit une valeur déterminant comment les métafichiers WMF contenant des métafichiers EMF intégrés doivent être rendus en C++."
type: docs
weight: 7000
url: /fr/cpp/aspose.words.saving/metafilerenderingoptions/get_useemfembeddedtowmf/
---
## MetafileRenderingOptions::get_UseEmfEmbeddedToWmf method


Obtient ou définit une valeur déterminant comment les métafichiers WMF contenant des métafichiers EMF intégrés doivent être rendus.

```cpp
bool Aspose::Words::Saving::MetafileRenderingOptions::get_UseEmfEmbeddedToWmf() const
```

## Remarques


Les fichiers WMF peuvent contenir des données EMF intégrées. MS Word utilise généralement des données EMF intégrées. GDI+ utilise toujours des données WMF.

Lorsque cette valeur est définie sur **true**, Aspose.Words utilise des données EMF intégrées lors du rendu.

Lorsque cette valeur est définie sur **false**, Aspose.Words utilise des données WMF lors du rendu.

Cette option n'est utilisée que lorsque le fichier métas est rendu en tant que graphiques vectoriels. Lorsque le fichier métas est rendu en bitmap, les données WMF sont toujours utilisées.

La valeur par défaut est **true**.
## Voir aussi

* Class [MetafileRenderingOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
