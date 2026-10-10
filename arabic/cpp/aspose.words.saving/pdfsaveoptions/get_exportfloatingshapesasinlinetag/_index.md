---
title: "طريقة Aspose::Words::Saving::PdfSaveOptions::get_ExportFloatingShapesAsInlineTag"
linktitle: "get_ExportFloatingShapesAsInlineTag"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Saving::PdfSaveOptions::get_ExportFloatingShapesAsInlineTag. تحصل أو تعيين قيمة تحدد ما إذا كانت الأشكال العائمة تُصدَّر كوسوم مضمنة في بنية المستند في C++."
type: docs
weight: 16500
url: /ar/cpp/aspose.words.saving/pdfsaveoptions/get_exportfloatingshapesasinlinetag/
---
## PdfSaveOptions::get_ExportFloatingShapesAsInlineTag method


يحصل أو يضبط قيمة تحدد ما إذا كانت الأشكال العائمة تُصدَّر كوسوم مضمنة في بنية المستند.

```cpp
bool Aspose::Words::Saving::PdfSaveOptions::get_ExportFloatingShapesAsInlineTag() const
```

## ملاحظات


القيمة الافتراضية هي **false** وسيتم تصدير الأشكال العائمة كوسوم على مستوى الكتلة، تُوضع بعد الفقرة التي تم تثبيتها فيها.

عند أن تكون القيمة **true**، سيتم تصدير الأشكال العائمة كوسوم مضمنة، تُوضع داخل الفقرة التي تم تثبيتها فيها.

يتم تجاهل هذه القيمة عندما يكون [ExportDocumentStructure](../get_exportdocumentstructure/) **false**.
## انظر أيضًا

* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
