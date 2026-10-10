---
title: "طريقة Aspose::Words::Saving::IDocumentSavingCallback::Notify"
linktitle: "Notify"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Saving::IDocumentSavingCallback::Notify. يتم استدعاؤها لإبلاغ عن تقدم حفظ المستند في C++."
type: docs
weight: 4000
url: /ar/cpp/aspose.words.saving/idocumentsavingcallback/notify/
---
## IDocumentSavingCallback::Notify method


يتم استدعاؤها لإبلاغ عن تقدم حفظ المستند.

```cpp
virtual void Aspose::Words::Saving::IDocumentSavingCallback::Notify(System::SharedPtr<Aspose::Words::Saving::DocumentSavingArgs> args)=0
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| args | System::SharedPtr\<Aspose::Words::Saving::DocumentSavingArgs\> | معامل للحدث. |
## ملاحظات


الاستخدامات الأساسية لهذه الواجهة هي السماح لكود التطبيق بالحصول على حالة التقدم وإلغاء عملية الحفظ.

يجب رمي استثناء من رد الاتصال الخاص بالتقدم لإلغاء العملية ويجب التقاطه في كود المستهلك.

## انظر أيضًا

* Class [DocumentSavingArgs](../../documentsavingargs/)
* Interface [IDocumentSavingCallback](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
