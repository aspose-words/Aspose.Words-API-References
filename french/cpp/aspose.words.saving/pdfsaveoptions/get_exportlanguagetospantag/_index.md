---
title: "Aspose::Words::Saving::PdfSaveOptions::get_ExportLanguageToSpanTag méthode"
linktitle: "get_ExportLanguageToSpanTag"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Saving::PdfSaveOptions::get_ExportLanguageToSpanTag méthode. Obtient ou définit une valeur déterminant s'il faut créer ou non une balise \"Span\" dans la structure du document pour exporter la langue du texte en C++."
type: docs
weight: 17000
url: /fr/cpp/aspose.words.saving/pdfsaveoptions/get_exportlanguagetospantag/
---
## PdfSaveOptions::get_ExportLanguageToSpanTag method


Obtient ou définit une valeur déterminant s'il faut créer ou non une balise "Span" dans la structure du document pour exporter la langue du texte.

```cpp
bool Aspose::Words::Saving::PdfSaveOptions::get_ExportLanguageToSpanTag() const
```

## Remarques


La valeur par défaut est **false** et l'attribut "Lang" est attaché à une séquence de contenu marqué dans le flux de contenu d'une page.

Lorsque la valeur est **true**, une balise "Span" est créée pour le texte avec une langue non par défaut et l'attribut "Lang" est attaché à cette balise.

Cette valeur est ignorée lorsque [ExportDocumentStructure](../get_exportdocumentstructure/) est **false**.
## Voir aussi

* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
