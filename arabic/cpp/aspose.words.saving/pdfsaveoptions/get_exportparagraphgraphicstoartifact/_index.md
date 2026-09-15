---
title: "طريقة Aspose::Words::Saving::PdfSaveOptions::get_ExportParagraphGraphicsToArtifact"
linktitle: "get_ExportParagraphGraphicsToArtifact"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Saving::PdfSaveOptions::get_ExportParagraphGraphicsToArtifact. يحصل على أو يعيّن قيمة تحدد ما إذا كان يجب وضع علامة على رسم الفقرة كقطعة أثرية في C++."
type: docs
weight: 17500
url: /ar/cpp/aspose.words.saving/pdfsaveoptions/get_exportparagraphgraphicstoartifact/
---
## PdfSaveOptions::get_ExportParagraphGraphicsToArtifact method


يحصل أو يضبط قيمة تحدد ما إذا كان يجب وضع علامة على رسم الفقرة كعنصر غير أساسي.

```cpp
bool Aspose::Words::Saving::PdfSaveOptions::get_ExportParagraphGraphicsToArtifact() const
```

## ملاحظات


القيمة الافتراضية هي **false** وسيتم وضع علامة على رسومات الفقرة (التسطير، تأكيد النص، إلخ) كـ "Span" في الهيكل المنطقي للمستند.

عند كون القيمة **true** سيتم وضع علامة على رسومات الفقرة كـ "Artifact".

يتم تجاهل هذه القيمة عندما يكون [ExportDocumentStructure](../get_exportdocumentstructure/) **false**.
## انظر أيضًا

* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
