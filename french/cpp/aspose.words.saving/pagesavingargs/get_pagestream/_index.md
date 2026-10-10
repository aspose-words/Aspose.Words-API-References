---
title: "Aspose::Words::Saving::PageSavingArgs::get_PageStream méthode"
linktitle: "get_PageStream"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Saving::PageSavingArgs::get_PageStream méthode. Permet de spécifier le flux où la page du document sera enregistrée en C++."
type: docs
weight: 6000
url: /fr/cpp/aspose.words.saving/pagesavingargs/get_pagestream/
---
## PageSavingArgs::get_PageStream method


Permet de spécifier le flux où la page du document sera enregistrée.

```cpp
System::SharedPtr<System::IO::Stream> Aspose::Words::Saving::PageSavingArgs::get_PageStream() const
```

## Remarques


Cette propriété vous permet d’enregistrer les pages de document dans des flux au lieu de fichiers.

La valeur par défaut est **null**. Lorsque cette propriété est **null**, la page du document sera enregistrée dans un fichier spécifié dans la propriété [PageFileName](../get_pagefilename/).

Si les deux [PageStream](./) et [PageFileName](../get_pagefilename/) sont définis, alors PageStream sera utilisé.

## Voir aussi

* Class [PageSavingArgs](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
