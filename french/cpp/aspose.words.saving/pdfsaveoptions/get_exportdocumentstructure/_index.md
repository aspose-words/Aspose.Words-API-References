---
title: "Méthode Aspose::Words::Saving::PdfSaveOptions::get_ExportDocumentStructure"
linktitle: "get_ExportDocumentStructure"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Saving::PdfSaveOptions::get_ExportDocumentStructure. Obtient ou définit une valeur déterminant s'il faut exporter ou non la structure du document dans C++."
type: docs
weight: 16000
url: /fr/cpp/aspose.words.saving/pdfsaveoptions/get_exportdocumentstructure/
---
## PdfSaveOptions::get_ExportDocumentStructure method


Obtient ou définit une valeur déterminant s'il faut exporter ou non la structure du document.

```cpp
bool Aspose::Words::Saving::PdfSaveOptions::get_ExportDocumentStructure() const
```

## Remarques


Cette valeur est ignorée lors de l'enregistrement en PDF/A-1a, PDF/A-2a et PDF/UA-1 car la structure du document est requise pour cette conformité.

Notez que l'exportation de la structure du document augmente considérablement la consommation de mémoire, en particulier pour les gros documents.
## Voir aussi

* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
