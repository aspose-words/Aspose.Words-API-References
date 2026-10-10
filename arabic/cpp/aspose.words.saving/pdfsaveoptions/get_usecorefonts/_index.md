---
title: "طريقة Aspose::Words::Saving::PdfSaveOptions::get_UseCoreFonts"
linktitle: "get_UseCoreFonts"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Saving::PdfSaveOptions::get_UseCoreFonts. تحصل أو تضبط قيمة تحدد ما إذا كان سيتم استبدال خطوط TrueType Arial، Times New Roman، Courier New و Symbol بخطوط PDF الأساسية من النوع 1 في C++."
type: docs
weight: 32000
url: /ar/cpp/aspose.words.saving/pdfsaveoptions/get_usecorefonts/
---
## PdfSaveOptions::get_UseCoreFonts method


يحصل أو يعيّن قيمة تحدد ما إذا كان يجب استبدال خطوط TrueType Arial و Times New Roman و Courier New و Symbol بخطوط PDF Type 1 الأساسية أم لا.

```cpp
bool Aspose::Words::Saving::PdfSaveOptions::get_UseCoreFonts() const
```

## ملاحظات


القيمة الافتراضية هي **false**. عندما يتم ضبط هذه القيمة إلى **true** يتم استبدال خطوط Arial، Times New Roman، Courier New و Symbol في مستند PDF بالخط الأساسي من النوع 1 المقابل.

خطوط PDF الأساسية، أو مقاييسها الخطية والخطوط البديلة المناسبة، يجب أن تكون متاحة لأي تطبيق عارض PDF.

هذا الإعداد يعمل فقط للنص المشفر بـ ANSI (Windows-1252). النص غير ANSI سيُكتب بخط TrueType مضمّن بغض النظر عن هذا الإعداد.

يتطلب التوافق مع PDF/A و PDF/UA تضمين جميع الخطوط. سيتم استخدام القيمة **false** تلقائيًا عند الحفظ إلى PDF/A و PDF/UA.

الخطوط الأساسية غير مدعومة عند الحفظ بصيغة PDF 2.0. سيتم استخدام القيمة **false** تلقائيًا عند الحفظ إلى PDF 2.0.

هذا الخيار له أولوية أعلى من خيار [FontEmbeddingMode](../get_fontembeddingmode/).
## انظر أيضًا

* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
