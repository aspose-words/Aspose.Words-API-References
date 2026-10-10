---
title: "Aspose::Words::Loading::IDocumentLoadingCallback::Notify metodu"
linktitle: "Notify"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Loading::IDocumentLoadingCallback::Notify metodu. Bu, C++'ta belge yükleme ilerlemesini bildirmek için çağrılır."
type: docs
weight: 4000
url: /tr/cpp/aspose.words.loading/idocumentloadingcallback/notify/
---
## IDocumentLoadingCallback::Notify method


Bu, belge yükleme ilerlemesi hakkında bildirim yapmak için çağrılır.

```cpp
virtual void Aspose::Words::Loading::IDocumentLoadingCallback::Notify(System::SharedPtr<Aspose::Words::Loading::DocumentLoadingArgs> args)=0
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| argümanlar | System::SharedPtr\<Aspose::Words::Loading::DocumentLoadingArgs\> | Olayın bir argümanı. |
## Açıklamalar


Bu arabirimin temel kullanımı, uygulama kodunun ilerleme durumunu almasını ve yükleme sürecini iptal etmesini sağlamaktır.

İptal için ilerleme geri çağırmasından bir istisna atılmalı ve tüketici kodunda yakalanmalıdır.

## Ayrıca Bakınız

* Class [DocumentLoadingArgs](../../documentloadingargs/)
* Interface [IDocumentLoadingCallback](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
