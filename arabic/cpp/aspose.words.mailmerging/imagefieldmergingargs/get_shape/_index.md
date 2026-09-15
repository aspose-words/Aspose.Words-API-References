---
title: "Aspose::Words::MailMerging::ImageFieldMergingArgs::get_Shape طريقة"
linktitle: "get_Shape"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::MailMerging::ImageFieldMergingArgs::get_Shape. تحدد الشكل الذي يجب على محرك دمج البريد إدراجه في المستند بلغة C++."
type: docs
weight: 7000
url: /ar/cpp/aspose.words.mailmerging/imagefieldmergingargs/get_shape/
---
## ImageFieldMergingArgs::get_Shape method


يحدد الشكل الذي يجب على محرك دمج البريد إدراجه في المستند.

```cpp
const System::SharedPtr<Aspose::Words::Drawing::Shape> & Aspose::Words::MailMerging::ImageFieldMergingArgs::get_Shape() const
```

## ملاحظات


عند تحديد هذه الخاصية، يتجاهل محرك دمج البريد جميع الخصائص الأخرى مثل [ImageFileName](../get_imagefilename/) أو [ImageStream](../get_imagestream/) ويقوم ببساطة بإدراج الشكل في المستند.

استخدم هذه الخاصية للتحكم الكامل في عملية دمج حقل دمج الصورة. على سبيل المثال، يمكنك تحديد [WrapType](../../../aspose.words.drawing/shapebase/get_wraptype/) أو أي خاصية شكل أخرى لضبط العقدة الناتجة بدقة. ومع ذلك، يرجى ملاحظة أنك مسؤول عن توفير محتوى الشكل.
## انظر أيضًا

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [ImageFieldMergingArgs](../)
* Namespace [Aspose::Words::MailMerging](../../)
* Library [Aspose.Words for C++](../../../)
