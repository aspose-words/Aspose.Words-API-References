---
title: "Aspose::Words::Saving::MetafileRenderingOptions::get_EmulateRenderingToSizeOnPage طريقة"
linktitle: "get_EmulateRenderingToSizeOnPage"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Saving::MetafileRenderingOptions::get_EmulateRenderingToSizeOnPage طريقة. يحصل أو يعيّن قيمة تحدد ما إذا كان تصيير ملف الميتا يحاكي عرض الملف وفقًا للحجم على الصفحة أو عرض الملف بحجمه الافتراضي في C++."
type: docs
weight: 4334
url: /ar/cpp/aspose.words.saving/metafilerenderingoptions/get_emulaterenderingtosizeonpage/
---
## MetafileRenderingOptions::get_EmulateRenderingToSizeOnPage method


يحصل أو يعيّن قيمة تحدد ما إذا كان تصيير ملف الميتا يحاكي عرض الملف وفقًا لحجمه على الصفحة أو عرضه بالحجم الافتراضي.

```cpp
bool Aspose::Words::Saving::MetafileRenderingOptions::get_EmulateRenderingToSizeOnPage() const
```

## ملاحظات


عند عرض ملفات الميتا في MS Word، قد يتم تحجيم بعض الرسومات وفقًا لحجم ملف الميتا الفعلي بالبكسل. أي أن التكبير قد يؤثر أيضًا على عرض ملف الميتا.

عند تعيين هذه القيمة إلى **true**، يقوم Aspose.Words بمحاكاة التصيير وفقًا لحجم ملف الميتا على الصفحة. يتم حساب الحجم بالبكسل من حجم ملف الميتا على الصفحة والـ [EmulateRenderingToSizeOnPageResolution](../get_emulaterenderingtosizeonpageresolution/) المحدد.

عند تعيين هذه القيمة إلى **false**، يقوم Aspose.Words بمحاكاة تصيير ملف الميتا إلى حجمه الافتراضي بالبكسل.

يُستخدم هذا الخيار فقط عندما يتم تصيير ملف الميتا كرسومات متجهة.

القيمة الافتراضية هي **true**.
## انظر أيضًا

* Class [MetafileRenderingOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
