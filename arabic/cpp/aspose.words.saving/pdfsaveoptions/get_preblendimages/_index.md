---
title: "طريقة Aspose::Words::Saving::PdfSaveOptions::get_PreblendImages"
linktitle: "get_PreblendImages"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Saving::PdfSaveOptions::get_PreblendImages. تحصل أو تعين قيمة تحدد ما إذا كان يجب دمج الصور الشفافة مسبقًا مع لون خلفية أسود في C++."
type: docs
weight: 27000
url: /ar/cpp/aspose.words.saving/pdfsaveoptions/get_preblendimages/
---
## PdfSaveOptions::get_PreblendImages method


يحصل أو يعيّن قيمة تحدد ما إذا كان يجب دمج الصور الشفافة مسبقًا مع لون الخلفية الأسود أم لا.

```cpp
bool Aspose::Words::Saving::PdfSaveOptions::get_PreblendImages() const
```

## ملاحظات


قد يؤدي دمج الصور مسبقًا إلى تحسين المظهر البصري لمستند PDF في Adobe Reader وإزالة عيوب التنعيم.

لكي يتم عرض الصور المدمجة مسبقًا بشكل صحيح، يجب أن يدعم تطبيق عارض PDF مدخل /Matte في قاموس صورة القناع الناعم. كما أن دمج الصور مسبقًا قد يقلل من أداء عرض PDF.

القيمة الافتراضية هي **false**.
## انظر أيضًا

* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
