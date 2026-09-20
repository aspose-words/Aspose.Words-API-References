---
title: "Método Aspose::Words::Saving::PdfSaveOptions::get_CustomPropertiesExport"
linktitle: "get_CustomPropertiesExport"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Saving::PdfSaveOptions::get_CustomPropertiesExport. Obtiene o establece un valor que determina la forma en que las CustomDocumentProperties se exportan al archivo PDF en C++."
type: docs
weight: 8000
url: /es/cpp/aspose.words.saving/pdfsaveoptions/get_custompropertiesexport/
---
## PdfSaveOptions::get_CustomPropertiesExport method


Obtiene o establece un valor que determina la forma en que [CustomDocumentProperties](../../../aspose.words/document/get_customdocumentproperties/) se exportan al archivo PDF.

```cpp
Aspose::Words::Saving::PdfCustomPropertiesExport Aspose::Words::Saving::PdfSaveOptions::get_CustomPropertiesExport() const
```

## Observaciones


El valor predeterminado es [None](../../pdfcustompropertiesexport/).

[Metadata](../../pdfcustompropertiesexport/) value is not supported when saving to PDF/A. [Standard](../../pdfcustompropertiesexport/) will be used instead for PDF/A-1 and PDF/A-2 and [None](../../pdfcustompropertiesexport/) for PDF/A-4.

[Standard](../../pdfcustompropertiesexport/) value is not supported when saving to PDF 2.0. [Metadata](../../pdfcustompropertiesexport/) will be used instead. 
## Ver también

* Enum [PdfCustomPropertiesExport](../../pdfcustompropertiesexport/)
* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
