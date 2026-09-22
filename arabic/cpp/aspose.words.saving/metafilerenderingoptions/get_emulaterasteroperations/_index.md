---
title: "Aspose::Words::Saving::MetafileRenderingOptions::get_EmulateRasterOperations طريقة"
linktitle: "get_EmulateRasterOperations"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Saving::MetafileRenderingOptions::get_EmulateRasterOperations طريقة. يحصل أو يعيّن قيمة تحدد ما إذا كان يجب محاكاة عمليات الراستر في C++."
type: docs
weight: 4000
url: /ar/cpp/aspose.words.saving/metafilerenderingoptions/get_emulaterasteroperations/
---
## MetafileRenderingOptions::get_EmulateRasterOperations method


يحصل أو يعيّن قيمة تحدد ما إذا كان يجب محاكاة عمليات الرستر أم لا.

```cpp
bool Aspose::Words::Saving::MetafileRenderingOptions::get_EmulateRasterOperations() const
```

## ملاحظات


يمكن استخدام عمليات الراستر المحددة في ملفات الميتا. لا يمكن تصييرها مباشرة إلى رسومات متجهة. تتطلب محاكاة عمليات الراستر تمثيلًا جزئيًا للراستر للرسومات المتجهة الناتجة مما قد يؤثر على أداء تصيير ملف الميتا.

عند تعيين هذه القيمة إلى **true**، يقوم Aspose.Words بمحاكاة عمليات الراستر. قد يكون الناتج جزئيًا مُمثلًا كراستر وقد يكون الأداء أبطأ.

عند تعيين هذه القيمة إلى **false**، لا يقوم Aspose.Words بمحاكاة عمليات الراستر. عندما يواجه [Aspose.Words](../../../aspose.words/) عملية راستر في ملف ميتا، يلجأ إلى تصيير ملف الميتا إلى صورة نقطية باستخدام نظام التشغيل.

يُستخدم هذا الخيار فقط عندما يتم تصيير ملف الميتا كرسومات متجهة.

القيمة الافتراضية هي **true**.
## انظر أيضًا

* Class [MetafileRenderingOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
