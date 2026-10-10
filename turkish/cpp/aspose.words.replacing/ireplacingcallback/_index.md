---
title: "Aspose::Words::Replacing::IReplacingCallback interface"
linktitle: "IReplacingCallback"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Replacing::IReplacingCallback arayüzü. C++'da bul ve değiştir işlemi sırasında çağrılacak kendi özel yönteminizi oluşturmak istiyorsanız bu arayüzü uygulayın."
type: docs
weight: 3000
url: /tr/cpp/aspose.words.replacing/ireplacingcallback/
---
## IReplacingCallback interface


Bir bul ve değiştirme işlemi sırasında çağrılacak kendi özel yönteminizi oluşturmak istiyorsanız bu arayüzü uygulayın.

```cpp
class IReplacingCallback : public virtual System::Object
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Replacing](./replacing/)(System::SharedPtr\<Aspose::Words::Replacing::ReplacingArgs\>) | Her bulunan eşleşme için, değiştirme işlemi yapılmadan hemen önce çağrılan kullanıcı tanımlı bir yöntem. |
| static [Type](./type/)() |  |
## Ayrıca Bakınız

* Namespace [Aspose::Words::Replacing](../)
* Library [Aspose.Words for C++](../../)
