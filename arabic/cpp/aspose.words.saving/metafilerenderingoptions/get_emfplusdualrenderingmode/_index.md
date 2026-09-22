---
title: "Aspose::Words::Saving::MetafileRenderingOptions::get_EmfPlusDualRenderingMode method"
linktitle: "get_EmfPlusDualRenderingMode"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Saving::MetafileRenderingOptions::get_EmfPlusDualRenderingMode method. يحصل أو يحدد قيمة تحدد كيفية عرض ملفات EMF+ Dual في C++."
type: docs
weight: 3000
url: /ar/cpp/aspose.words.saving/metafilerenderingoptions/get_emfplusdualrenderingmode/
---
## MetafileRenderingOptions::get_EmfPlusDualRenderingMode method


يحصل أو يعيّن قيمة تحدد كيفية تصيير ملفات EMF+ Dual.

```cpp
Aspose::Words::Saving::EmfPlusDualRenderingMode Aspose::Words::Saving::MetafileRenderingOptions::get_EmfPlusDualRenderingMode() const
```

## ملاحظات


تحتوي ملفات EMF+ Dual على كل من أجزاء EMF+ و EMF. يقوم MS Word و GDI+ دائمًا بعرض جزء EMF+. لا يدعم Aspose.Words حاليًا جميع سجلات EMF+ بشكل كامل، وفي بعض الحالات يبدو نتيجة عرض جزء EMF أفضل من نتيجة عرض جزء EMF+.

يُستخدم هذا الخيار فقط عندما يتم عرض ملف الميتا كرسومات متجهة. عندما يتم عرض ملف الميتا إلى صورة نقطية، يُستخدم دائمًا جزء EMF+.

القيمة الافتراضية هي [EmfPlusWithFallback](../../emfplusdualrenderingmode/).
## انظر أيضًا

* Enum [EmfPlusDualRenderingMode](../../emfplusdualrenderingmode/)
* Class [MetafileRenderingOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
