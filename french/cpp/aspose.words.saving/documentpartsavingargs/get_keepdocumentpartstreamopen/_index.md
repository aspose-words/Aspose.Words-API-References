---
title: "Aspose::Words::Saving::DocumentPartSavingArgs::get_KeepDocumentPartStreamOpen méthode"
linktitle: "get_KeepDocumentPartStreamOpen"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Saving::DocumentPartSavingArgs::get_KeepDocumentPartStreamOpen méthode. Spécifie si Aspose.Words doit garder le flux ouvert ou le fermer après l'enregistrement d'une partie de document en C++."
type: docs
weight: 5000
url: /fr/cpp/aspose.words.saving/documentpartsavingargs/get_keepdocumentpartstreamopen/
---
## DocumentPartSavingArgs::get_KeepDocumentPartStreamOpen method


Spécifie si Aspose.Words doit garder le flux ouvert ou le fermer après l'enregistrement d'une partie du document.

```cpp
bool Aspose::Words::Saving::DocumentPartSavingArgs::get_KeepDocumentPartStreamOpen() const
```

## Remarques


La valeur par défaut est **false** et Aspose.Words fermera le flux que vous avez fourni dans la propriété [DocumentPartStream](../get_documentpartstream/) après avoir écrit une partie de document dedans. Spécifiez **true** pour garder le flux ouvert. Veuillez noter que le flux de sortie principal fourni lors de l'appel à [Save()](../) ou [Save()](../) ne sera jamais fermé par Aspose.Words même si [KeepDocumentPartStreamOpen](./) est défini sur **false**.

## Voir aussi

* Class [DocumentPartSavingArgs](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
