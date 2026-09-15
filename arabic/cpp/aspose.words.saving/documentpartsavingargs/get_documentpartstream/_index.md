---
title: "طريقة Aspose::Words::Saving::DocumentPartSavingArgs::get_DocumentPartStream"
linktitle: "get_DocumentPartStream"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Saving::DocumentPartSavingArgs::get_DocumentPartStream. يسمح بتحديد الدفق الذي سيتم حفظ جزء المستند إليه في C++."
type: docs
weight: 4000
url: /ar/cpp/aspose.words.saving/documentpartsavingargs/get_documentpartstream/
---
## DocumentPartSavingArgs::get_DocumentPartStream method


يسمح بتحديد الدفق حيث سيتم حفظ جزء المستند.

```cpp
System::SharedPtr<System::IO::Stream> Aspose::Words::Saving::DocumentPartSavingArgs::get_DocumentPartStream() const
```

## ملاحظات


هذه الخاصية تسمح لك بحفظ أجزاء المستند إلى تدفقات بدلاً من ملفات أثناء تصدير HTML.

القيمة الافتراضية هي **null**. عندما تكون هذه الخاصية **null**، سيتم حفظ جزء المستند إلى ملف محدد في خاصية [DocumentPartFileName](../get_documentpartfilename/).

عند طلب الحفظ إلى تدفق بصيغة HTML عبر [Save()](../) أو [Save()](../) وكان الجزء الأول من المستند على وشك الحفظ، تقترح Aspose.Words هنا تدفق الإخراج الرئيسي الذي تم تمريره في البداية من قبل المستدعي.

عند الحفظ إلى صيغة EPUB التي هي صيغة حاوية تعتمد على HTML، لا يمكن تحديد [DocumentPartStream](./) لأن جميع الأجزاء الفرعية سيتم تضمينها في حزمة إخراج واحدة.

## انظر أيضًا

* Class [DocumentPartSavingArgs](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
