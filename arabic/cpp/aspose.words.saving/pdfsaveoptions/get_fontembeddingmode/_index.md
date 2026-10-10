---
title: "Aspose::Words::Saving::PdfSaveOptions::get_FontEmbeddingMode طريقة"
linktitle: "get_FontEmbeddingMode"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Saving::PdfSaveOptions::get_FontEmbeddingMode طريقة. يحدد وضع تضمين الخط في C++."
type: docs
weight: 18000
url: /ar/cpp/aspose.words.saving/pdfsaveoptions/get_fontembeddingmode/
---
## PdfSaveOptions::get_FontEmbeddingMode method


يحدد وضع تضمين الخط.

```cpp
Aspose::Words::Saving::PdfFontEmbeddingMode Aspose::Words::Saving::PdfSaveOptions::get_FontEmbeddingMode() const
```

## ملاحظات


القيمة الافتراضية هي [EmbedAll](../../pdffontembeddingmode/).

هذا الإعداد يعمل فقط للنص بتشفير ANSI (Windows-1252). إذا كان المستند يحتوي على نص غير ANSI فسيتم تضمين الخطوط المقابلة بغض النظر عن هذا الإعداد.

يتطلب الامتثال لـ PDF/A و PDF/UA تضمين جميع الخطوط. سيتم استخدام القيمة [EmbedAll](../../pdffontembeddingmode/) تلقائيًا عند الحفظ إلى PDF/A و PDF/UA.
## انظر أيضًا

* Enum [PdfFontEmbeddingMode](../../pdffontembeddingmode/)
* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
