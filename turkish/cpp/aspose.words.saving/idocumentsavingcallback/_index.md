---
title: "Aspose::Words::Saving::IDocumentSavingCallback arayüzü"
linktitle: "IDocumentSavingCallback"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::IDocumentSavingCallback arayüzü. Bu arayüzü, C++'ta bir belge kaydedilirken kendi özel yönteminizi çağırmak istiyorsanız uygulayın."
type: docs
weight: 41000
url: /tr/cpp/aspose.words.saving/idocumentsavingcallback/
---
## IDocumentSavingCallback interface


Bir belgeyi kaydederken kendi özel yönteminizi çağırmak istiyorsanız bu arabirimi uygulayın.

```cpp
class IDocumentSavingCallback : public virtual System::Object
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Notify](./notify/)(System::SharedPtr\<Aspose::Words::Saving::DocumentSavingArgs\>) | Bu, belge kaydetme ilerlemesi hakkında bildirim yapmak için çağrılır. |
| static [Type](./type/)() |  |
## Ayrıca Bakınız

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
