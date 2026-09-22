---
title: "Aspose::Words::Saving::PdfSaveOptions::get_CustomPropertiesExport method"
linktitle: "get_CustomPropertiesExport"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Saving::PdfSaveOptions::get_CustomPropertiesExport method. يحصل أو يعيّن قيمة تحدد طريقة تصدير CustomDocumentProperties إلى ملف PDF في C++."
type: docs
weight: 8000
url: /ar/cpp/aspose.words.saving/pdfsaveoptions/get_custompropertiesexport/
---
## PdfSaveOptions::get_CustomPropertiesExport method


يحصل أو يعيّن قيمة تحدد طريقة تصدير [CustomDocumentProperties](../../../aspose.words/document/get_customdocumentproperties/) إلى ملف PDF.

```cpp
Aspose::Words::Saving::PdfCustomPropertiesExport Aspose::Words::Saving::PdfSaveOptions::get_CustomPropertiesExport() const
```

## ملاحظات


القيمة الافتراضية هي [None](../../pdfcustompropertiesexport/).

[Metadata](../../pdfcustompropertiesexport/) value is not supported when saving to PDF/A. [Standard](../../pdfcustompropertiesexport/) will be used instead for PDF/A-1 and PDF/A-2 and [None](../../pdfcustompropertiesexport/) for PDF/A-4.

[Standard](../../pdfcustompropertiesexport/) value is not supported when saving to PDF 2.0. [Metadata](../../pdfcustompropertiesexport/) will be used instead. 
## انظر أيضًا

* Enum [PdfCustomPropertiesExport](../../pdfcustompropertiesexport/)
* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
