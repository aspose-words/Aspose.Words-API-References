---
title: "Aspose::Words::Saving::PdfSaveOptions::get_ExportLanguageToSpanTag طريقة"
linktitle: "get_ExportLanguageToSpanTag"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Saving::PdfSaveOptions::get_ExportLanguageToSpanTag طريقة. يحصل على أو يحدد قيمة تحدد ما إذا كان سيتم إنشاء وسم \\\"Span\\\" في بنية المستند لتصدير لغة النص في C++."
type: docs
weight: 17000
url: /ar/cpp/aspose.words.saving/pdfsaveoptions/get_exportlanguagetospantag/
---
## PdfSaveOptions::get_ExportLanguageToSpanTag method


يحصل أو يضبط قيمة تحدد ما إذا كان يجب إنشاء وسم "Span" في بنية المستند لتصدير لغة النص أم لا.

```cpp
bool Aspose::Words::Saving::PdfSaveOptions::get_ExportLanguageToSpanTag() const
```

## ملاحظات


القيمة الافتراضية هي **false** و سمة \"Lang\" مرفقة بتسلسل محتوى محدد في تدفق محتوى الصفحة.

عند أن تكون القيمة **true** يتم إنشاء وسم \"Span\" للنص ذو اللغة غير الافتراضية وتُرفق سمة \"Lang\" بهذا الوسم.

يتم تجاهل هذه القيمة عندما يكون [ExportDocumentStructure](../get_exportdocumentstructure/) **false**.
## انظر أيضًا

* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
