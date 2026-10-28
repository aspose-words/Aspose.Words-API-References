---
title: Aspose::Words::Saving::PdfSaveOptions::set_CustomPropertiesExport method
linktitle: set_CustomPropertiesExport
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::PdfSaveOptions::set_CustomPropertiesExport method. Sets a value determining the way CustomDocumentProperties are exported to PDF file in C++.'
type: docs
weight: 41000
url: /cpp/aspose.words.saving/pdfsaveoptions/set_custompropertiesexport/
---
## PdfSaveOptions::set_CustomPropertiesExport method


Sets a value determining the way [CustomDocumentProperties](../../../aspose.words/document/get_customdocumentproperties/) are exported to PDF file.

```cpp
void Aspose::Words::Saving::PdfSaveOptions::set_CustomPropertiesExport(Aspose::Words::Saving::PdfCustomPropertiesExport value)
```

## Remarks


Default value is [None](../../pdfcustompropertiesexport/).

[Metadata](../../pdfcustompropertiesexport/) value is not supported when saving to PDF/A. [Standard](../../pdfcustompropertiesexport/) will be used instead for PDF/A-1 and PDF/A-2 and [None](../../pdfcustompropertiesexport/) for PDF/A-4.

[Standard](../../pdfcustompropertiesexport/) value is not supported when saving to PDF 2.0. [Metadata](../../pdfcustompropertiesexport/) will be used instead.
## See Also

* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
