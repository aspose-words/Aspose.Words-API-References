---
title: "Aspose::Words::Loading::IDocumentLoadingCallback interface"
linktitle: "IDocumentLoadingCallback"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Loading::IDocumentLoadingCallback arayüzü. Bu arayüzü, C++'da bir belge yüklenirken çağrılan kendi özel yönteminizi oluşturmak istiyorsanız uygulayın."
type: docs
weight: 10000
url: /tr/cpp/aspose.words.loading/idocumentloadingcallback/
---
## IDocumentLoadingCallback interface


Bir belge yüklenirken çağrılan kendi özel yönteminizi istiyorsanız bu arayüzü uygulayın.

```cpp
class IDocumentLoadingCallback : public virtual System::Object
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Notify](./notify/)(System::SharedPtr\<Aspose::Words::Loading::DocumentLoadingArgs\>) | Bu, belge yükleme ilerlemesi hakkında bildirim yapmak için çağrılır. |
| static [Type](./type/)() |  |
## Ayrıca Bakınız

* Namespace [Aspose::Words::Loading](../)
* Library [Aspose.Words for C++](../../)
