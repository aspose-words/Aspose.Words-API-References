---
title: "طريقة Aspose::Words::Saving::PdfSaveOptions::get_InterpolateImages"
linktitle: "get_InterpolateImages"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Saving::PdfSaveOptions::get_InterpolateImages. علم يحدد ما إذا كان يجب أن يقوم القارئ المتوافق بتنفيذ استيفاء الصورة. عندما يتم تحديد **false**، لا يتم كتابة العلم إلى مستند الإخراج ويُستخدم السلوك الافتراضي للقارئ بدلاً من ذلك في C++."
type: docs
weight: 22000
url: /ar/cpp/aspose.words.saving/pdfsaveoptions/get_interpolateimages/
---
## PdfSaveOptions::get_InterpolateImages method


علامة تشير إلى ما إذا كان يجب أن يقوم القارئ المتوافق بإجراء استيفاء الصورة. عندما يتم تحديد **false**، لا تُكتب العلامة إلى المستند الناتج ويُستخدم السلوك الافتراضي للقارئ بدلاً من ذلك.

```cpp
bool Aspose::Words::Saving::PdfSaveOptions::get_InterpolateImages() const
```

## ملاحظات


عندما تكون دقة الصورة المصدر أقل بكثير من دقة جهاز الإخراج، يغطي كل عينة مصدر العديد من بكسلات الجهاز. نتيجة لذلك، قد تظهر الصور متعرجة أو متكتلة. يمكن تقليل هذه العيوب البصرية عن طريق تطبيق خوارزمية استيفاء الصورة أثناء العرض. بدلاً من تلوين جميع البكسلات التي تغطيها عينة المصدر بنفس اللون، يحاول استيفاء الصورة إنتاج انتقال سلس بين قيم العينات المتجاورة.

قد يختار القارئ المتوافق عدم تنفيذ هذه الميزة في PDF، أو قد يستخدم أي تنفيذ محدد للاستيفاء يرغب فيه.

القيمة الافتراضية هي **false**.

يُحظر علم الاستيفاء وفقًا لتوافق PDF/A. سيتم استخدام القيمة **false** تلقائيًا عند الحفظ إلى PDF/A.
## انظر أيضًا

* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
