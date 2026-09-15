---
title: "طريقة Aspose::Words::Saving::ImageSavingArgs::get_ImageStream"
linktitle: "get_ImageStream"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Saving::ImageSavingArgs::get_ImageStream. يسمح بتحديد الدفق الذي سيتم حفظ الصورة إليه في C++."
type: docs
weight: 5000
url: /ar/cpp/aspose.words.saving/imagesavingargs/get_imagestream/
---
## ImageSavingArgs::get_ImageStream method


يسمح بتحديد الدفق الذي سيتم حفظ الصورة فيه.

```cpp
System::SharedPtr<System::IO::Stream> Aspose::Words::Saving::ImageSavingArgs::get_ImageStream() const
```

## ملاحظات


تتيح لك هذه الخاصية حفظ الصور إلى تدفقات بدلاً من الملفات أثناء HTML.

القيمة الافتراضية هي **null**. عندما تكون هذه الخاصية **null**، سيتم حفظ الصورة إلى ملف محدد في الخاصية [ImageFileName](../get_imagefilename/).

باستخدام [IImageSavingCallback](../../iimagesavingcallback/) لا يمكنك استبدال صورة بأخرى. إنها مخصصة فقط للتحكم في الموقع الذي تُحفظ فيه الصور.

## انظر أيضًا

* Class [ImageSavingArgs](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
