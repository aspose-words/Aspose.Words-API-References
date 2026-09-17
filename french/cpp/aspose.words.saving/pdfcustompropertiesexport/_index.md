---
title: "Aspose::Words::Saving::PdfCustomPropertiesExport enum"
linktitle: "PdfCustomPropertiesExport"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Saving::PdfCustomPropertiesExport enum. Spécifie la façon dont les CustomDocumentProperties sont exportées vers le fichier PDF en C++."
type: docs
weight: 74000
url: /fr/cpp/aspose.words.saving/pdfcustompropertiesexport/
---
## PdfCustomPropertiesExport enum


Spécifie la façon dont les [CustomDocumentProperties](../../aspose.words/document/get_customdocumentproperties/) sont exportées vers le fichier PDF.

```cpp
enum class PdfCustomPropertiesExport
```

### Valeurs

| Nom | Valeur | Description |
| --- | --- | --- |
| None | 0 | Aucune propriété personnalisée n'est exportée. |
| Standard | 1 | Les propriétés personnalisées sont exportées comme entrées dans le dictionnaire /Info. Les propriétés personnalisées portant les noms suivants ne sont pas exportées : "Title", "Author", "Subject", "Keywords", "Creator", "Producer", "CreationDate", "ModDate", "Trapped". |
| Métadonnées | 2 | Les propriétés personnalisées sont des métadonnées. |

## Voir aussi

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
