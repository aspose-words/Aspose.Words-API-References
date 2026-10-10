---
title: "طريقة Aspose::Words::Saving::PageSavingArgs::get_PageStream"
linktitle: "get_PageStream"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Saving::PageSavingArgs::get_PageStream. تسمح بتحديد الدفق الذي سيتم حفظ صفحة المستند إليه في C++."
type: docs
weight: 6000
url: /ar/cpp/aspose.words.saving/pagesavingargs/get_pagestream/
---
## PageSavingArgs::get_PageStream method


يسمح بتحديد الدفق حيث سيتم حفظ صفحة المستند.

```cpp
System::SharedPtr<System::IO::Stream> Aspose::Words::Saving::PageSavingArgs::get_PageStream() const
```

## ملاحظات


هذه الخاصية تسمح لك بحفظ صفحات المستند إلى تدفقات بدلاً من ملفات.

القيمة الافتراضية هي **null**. عندما تكون هذه الخاصية **null**، سيتم حفظ صفحة المستند إلى ملف محدد في الخاصية [PageFileName](../get_pagefilename/).

إذا تم تعيين كل من [PageStream](./) و [PageFileName](../get_pagefilename/)، فسيتم استخدام PageStream.

## انظر أيضًا

* Class [PageSavingArgs](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
