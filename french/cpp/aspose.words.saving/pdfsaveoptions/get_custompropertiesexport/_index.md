---
title: "Aspose::Words::Saving::PdfSaveOptions::get_CustomPropertiesExport méthode"
linktitle: "get_CustomPropertiesExport"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Saving::PdfSaveOptions::get_CustomPropertiesExport méthode. Obtient ou définit une valeur déterminant la façon dont les CustomDocumentProperties sont exportées vers le fichier PDF en C++."
type: docs
weight: 8000
url: /fr/cpp/aspose.words.saving/pdfsaveoptions/get_custompropertiesexport/
---
## PdfSaveOptions::get_CustomPropertiesExport method


Obtient ou définit une valeur déterminant la façon dont [CustomDocumentProperties](../../../aspose.words/document/get_customdocumentproperties/) sont exportées vers le fichier PDF.

```cpp
Aspose::Words::Saving::PdfCustomPropertiesExport Aspose::Words::Saving::PdfSaveOptions::get_CustomPropertiesExport() const
```

## Remarques


La valeur par défaut est [None](../../pdfcustompropertiesexport/).

[Metadata](../../pdfcustompropertiesexport/) value is not supported when saving to PDF/A. [Standard](../../pdfcustompropertiesexport/) will be used instead for PDF/A-1 and PDF/A-2 and [None](../../pdfcustompropertiesexport/) for PDF/A-4.

[Standard](../../pdfcustompropertiesexport/) value is not supported when saving to PDF 2.0. [Metadata](../../pdfcustompropertiesexport/) will be used instead. 
## Voir aussi

* Enum [PdfCustomPropertiesExport](../../pdfcustompropertiesexport/)
* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
