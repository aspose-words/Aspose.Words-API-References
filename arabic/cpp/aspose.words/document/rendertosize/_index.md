---
title: "Aspose::Words::Document::RenderToSize طريقة"
linktitle: "RenderToSize"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Document::RenderToSize طريقة. تُظهر صفحة المستند في كائن Graphics بحجم محدد في C++."
type: docs
weight: 71000
url: /ar/cpp/aspose.words/document/rendertosize/
---
## Document::RenderToSize method


يرسم صفحة المستند في كائن **Graphics** إلى حجم محدد.

```cpp
float Aspose::Words::Document::RenderToSize(int32_t pageIndex, const System::SharedPtr<System::Drawing::Graphics> &graphics, float x, float y, float width, float height)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| pageIndex | int32_t | مؤشر الصفحة بدءًا من الصفر. |
| graphics | const System::SharedPtr\<System::Drawing::Graphics\>\& | الكائن الذي يتم الرسم إليه. |
| x | float | الإحداثي X (بوحدات العالم) للزاوية العلوية اليسرى للصفحة المُرَسَمة. |
| y | float | الإحداثي Y (بوحدات العالم) للزاوية العلوية اليسرى للصفحة المُرَسَمة. |
| العرض | float | العرض الأقصى (بوحدات العالم) الذي يمكن أن يشغله الصفحة المُعالجة. |
| الارتفاع | float | الارتفاع الأقصى (بوحدات العالم) الذي يمكن أن يشغله الصفحة المُعالجة. |

### ReturnValue

المقياس الذي تم حسابه تلقائيًا للصفحة المُعالجة لتتناسب مع الحجم المحدد.

## انظر أيضًا

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
