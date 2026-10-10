---
title: "طريقة Aspose::Words::Saving::ImageSavingArgs::get_CurrentShape"
linktitle: "get_CurrentShape"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Saving::ImageSavingArgs::get_CurrentShape. تحصل على كائن ShapeBase المقابل للشكل أو مجموعة الأشكال التي ستُحفظ قريبًا في C++."
type: docs
weight: 2000
url: /ar/cpp/aspose.words.saving/imagesavingargs/get_currentshape/
---
## ImageSavingArgs::get_CurrentShape method


تحصل على كائن [ShapeBase](../../../aspose.words.drawing/shapebase/) المقابل للشكل أو مجموعة الأشكال التي ستُحفظ قريبًا.

```cpp
System::SharedPtr<Aspose::Words::Drawing::ShapeBase> Aspose::Words::Saving::ImageSavingArgs::get_CurrentShape() const
```

## ملاحظات


[IImageSavingCallback](../../iimagesavingcallback/) can be fired while saving either a shape or a group shape. That's why the property has [ShapeBase](../../../aspose.words.drawing/shapebase/) type. You can check whether it's a group shape comparing [ShapeType](../../../aspose.words.drawing/shapebase/get_shapetype/) with [Group](../../../aspose.words.drawing/shapetype/) or by casting it to one of derived classes: [Shape](../../../aspose.words.drawing/shape/) or [GroupShape](../../../aspose.words.drawing/groupshape/).

يستخدم Aspose.Words اسم ملف المستند ورقمًا فريدًا لإنشاء اسم ملف فريد لكل صورة موجودة في المستند. يمكنك استخدام الخاصية [CurrentShape](./) لإنشاء اسم ملف \"أفضل\" من خلال فحص خصائص الشكل مثل [Title](../../../aspose.words.drawing/imagedata/get_title/) (للشكل فقط)، [SourceFullName](../../../aspose.words.drawing/imagedata/get_sourcefullname/) (للشكل فقط) و[Name](../../../aspose.words.drawing/shapebase/get_name/). بالطبع يمكنك بناء أسماء الملفات باستخدام أي خصائص أو معايير أخرى ولكن لاحظ أن أسماء الملفات الفرعية يجب أن تكون فريدة داخل عملية التصدير.

قد تكون بعض الصور في المستند غير متاحة. للتحقق من توفر الصورة استخدم الخاصية [IsImageAvailable](../get_isimageavailable/).
## انظر أيضًا

* Class [ShapeBase](../../../aspose.words.drawing/shapebase/)
* Class [ImageSavingArgs](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
