---
title: "طريقة Aspose::Words::Saving::ImageSavingArgs::get_IsImageAvailable"
linktitle: "get_IsImageAvailable"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Saving::ImageSavingArgs::get_IsImageAvailable. تُعيد true إذا كانت الصورة الحالية متاحة للتصدير في C++."
type: docs
weight: 6000
url: /ar/cpp/aspose.words.saving/imagesavingargs/get_isimageavailable/
---
## ImageSavingArgs::get_IsImageAvailable method


يرجع **true** إذا كانت الصورة الحالية متاحة للتصدير.

```cpp
bool Aspose::Words::Saving::ImageSavingArgs::get_IsImageAvailable() const
```

## ملاحظات


بعض الصور في المستند قد تكون غير متاحة، على سبيل المثال، لأن الصورة مرتبطة والرابط غير قابل للوصول أو لا يشير إلى صورة صالحة. في هذه الحالة يقوم Aspose.Words بتصدير أيقونة بعلامة صليب أحمر. هذه الخاصية تُعيد **true** إذا كانت الصورة الأصلية متاحة؛ تُعيد **false** إذا كانت الصورة الأصلية غير متاحة وسيتم تقديم أيقونة \"بدون صورة\" للحفظ.

عند حفظ شكل مجموعة أو شكل لا يتطلب أي صورة، تكون هذه الخاصية دائمًا **true**.

## انظر أيضًا

* Class [ImageSavingArgs](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
