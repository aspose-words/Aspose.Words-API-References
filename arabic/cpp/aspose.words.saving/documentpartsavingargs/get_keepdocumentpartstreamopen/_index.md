---
title: "طريقة Aspose::Words::Saving::DocumentPartSavingArgs::get_KeepDocumentPartStreamOpen"
linktitle: "get_KeepDocumentPartStreamOpen"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Saving::DocumentPartSavingArgs::get_KeepDocumentPartStreamOpen. تحدد ما إذا كان يجب على Aspose.Words إبقاء الدفق مفتوحًا أو إغلاقه بعد حفظ جزء من المستند في C++."
type: docs
weight: 5000
url: /ar/cpp/aspose.words.saving/documentpartsavingargs/get_keepdocumentpartstreamopen/
---
## DocumentPartSavingArgs::get_KeepDocumentPartStreamOpen method


يحدد ما إذا كان يجب على Aspose.Words إبقاء الدفق مفتوحًا أو إغلاقه بعد حفظ جزء المستند.

```cpp
bool Aspose::Words::Saving::DocumentPartSavingArgs::get_KeepDocumentPartStreamOpen() const
```

## ملاحظات


القيمة الافتراضية هي **false** وستقوم Aspose.Words بإغلاق الدفق الذي قدمته في الخاصية [DocumentPartStream](../get_documentpartstream/) بعد كتابة جزء من المستند فيه. حدد **true** لإبقاء الدفق مفتوحًا. يرجى ملاحظة أن الدفق الرئيسي للإخراج المقدم في استدعاء [Save()](../) أو [Save()](../) لن يتم إغلاقه أبدًا بواسطة Aspose.Words حتى إذا تم تعيين [KeepDocumentPartStreamOpen](./) إلى **false**.

## انظر أيضًا

* Class [DocumentPartSavingArgs](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
