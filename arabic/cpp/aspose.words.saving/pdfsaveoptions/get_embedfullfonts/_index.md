---
title: "طريقة Aspose::Words::Saving::PdfSaveOptions::get_EmbedFullFonts"
linktitle: "get_EmbedFullFonts"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Saving::PdfSaveOptions::get_EmbedFullFonts. يتحكم في كيفية تضمين الخطوط في مستندات PDF الناتجة في C++."
type: docs
weight: 14000
url: /ar/cpp/aspose.words.saving/pdfsaveoptions/get_embedfullfonts/
---
## PdfSaveOptions::get_EmbedFullFonts method


يتحكم في كيفية تضمين الخطوط في مستندات PDF الناتجة.

```cpp
bool Aspose::Words::Saving::PdfSaveOptions::get_EmbedFullFonts() const
```

## ملاحظات


القيمة الافتراضية هي **false**، مما يعني أنه يتم تقليل الخطوط قبل التضمين. التقليل مفيد إذا كنت تريد الحفاظ على حجم الملف الناتج أصغر. التقليل يزيل جميع الأحرف غير المستخدمة من الخط.

عند ضبط هذه القيمة إلى **true**، يتم تضمين ملف الخط بالكامل في PDF دون تقليل. سيؤدي ذلك إلى ملفات ناتجة أكبر، لكنه قد يكون خيارًا مفيدًا عندما تريد تعديل PDF الناتج لاحقًا (مثال: إضافة نص إضافي).

بعض الخطوط كبيرة (عدة ميغابايت) وتضمينها دون تقليل سيؤدي إلى مستندات ناتجة كبيرة.
## انظر أيضًا

* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
