---
title: "Aspose::Words::Saving::IDocumentSavingCallback::Notify yöntemi"
linktitle: "Notify"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::IDocumentSavingCallback::Notify yöntemi. Bu, C++'ta belge kaydetme ilerlemesini bildirmek için çağrılır."
type: docs
weight: 4000
url: /tr/cpp/aspose.words.saving/idocumentsavingcallback/notify/
---
## IDocumentSavingCallback::Notify method


Bu, belge kaydetme ilerlemesi hakkında bildirim yapmak için çağrılır.

```cpp
virtual void Aspose::Words::Saving::IDocumentSavingCallback::Notify(System::SharedPtr<Aspose::Words::Saving::DocumentSavingArgs> args)=0
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| argümanlar | System::SharedPtr\<Aspose::Words::Saving::DocumentSavingArgs\> | Olayın bir argümanı. |
## Açıklamalar


Bu arayüzün temel kullanımları, uygulama kodunun ilerleme durumunu almasını ve kaydetme sürecini iptal etmesini sağlamaktır.

İptal için ilerleme geri çağırmasından bir istisna atılmalı ve tüketici kodunda yakalanmalıdır.

## Ayrıca Bakınız

* Class [DocumentSavingArgs](../../documentsavingargs/)
* Interface [IDocumentSavingCallback](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
