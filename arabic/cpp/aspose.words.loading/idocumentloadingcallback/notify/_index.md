---
title: "طريقة Aspose::Words::Loading::IDocumentLoadingCallback::Notify"
linktitle: "Notify"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Loading::IDocumentLoadingCallback::Notify. يتم استدعاؤها لإبلاغ عن تقدم تحميل المستند في C++."
type: docs
weight: 4000
url: /ar/cpp/aspose.words.loading/idocumentloadingcallback/notify/
---
## IDocumentLoadingCallback::Notify method


يُستدعى هذا لإبلاغ عن تقدم تحميل المستند.

```cpp
virtual void Aspose::Words::Loading::IDocumentLoadingCallback::Notify(System::SharedPtr<Aspose::Words::Loading::DocumentLoadingArgs> args)=0
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| args | System::SharedPtr\<Aspose::Words::Loading::DocumentLoadingArgs\> | معامل للحدث. |
## ملاحظات


الاستخدامات الأساسية لهذه الواجهة هي السماح لكود التطبيق بالحصول على حالة التقدم وإلغاء عملية التحميل.

يجب رمي استثناء من رد الاتصال الخاص بالتقدم لإلغاء العملية ويجب التقاطه في كود المستهلك.

## انظر أيضًا

* Class [DocumentLoadingArgs](../../documentloadingargs/)
* Interface [IDocumentLoadingCallback](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
