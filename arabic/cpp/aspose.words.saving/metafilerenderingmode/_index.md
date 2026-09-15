---
title: "Aspose::Words::Saving::MetafileRenderingMode enum"
linktitle: "MetafileRenderingMode"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Saving::MetafileRenderingMode enum. يحدد كيف يجب على Aspose.Words أن يعرض ملفات WMF و EMF في C++."
type: docs
weight: 69000
url: /ar/cpp/aspose.words.saving/metafilerenderingmode/
---
## MetafileRenderingMode enum


يحدد كيفية عرض Aspose.Words لملفات WMF و EMF.

```cpp
enum class MetafileRenderingMode
```

### القيم

| الاسم | القيمة | الوصف |
| --- | --- | --- |
| VectorWithFallback | 0 | تحاول Aspose.Words عرض ملف تعريف كرسومات متجهية. إذا لم تستطع Aspose.Words عرض بعض سجلات ملف التعريف بشكل صحيح كرسومات متجهية فستعرض هذا الملف كصورة نقطية. |
| Vector | 1 | Aspose.Words يعرض ملفًا تعريفياً كرسومات متجهة. |
| صورة نقطية | 2 | Aspose.Words يستدعي GDI+ لعرض ملف تعريف إلى صورة نقطية ثم يحفظ الصورة النقطية في المستند الناتج. |

## انظر أيضًا

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
