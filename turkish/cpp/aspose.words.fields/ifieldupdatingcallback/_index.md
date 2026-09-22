---
title: "Aspose::Words::Fields::IFieldUpdatingCallback arayüzü"
linktitle: "IFieldUpdatingCallback"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fields::IFieldUpdatingCallback arayüzü. Bu arayüzü, C++'ta bir alan güncellemesi sırasında kendi özel yöntemlerinizin çağrılmasını istiyorsanız uygulayın."
type: docs
weight: 123000
url: /tr/cpp/aspose.words.fields/ifieldupdatingcallback/
---
## IFieldUpdatingCallback interface


Alan güncellemesi sırasında kendi özel yöntemlerinizin çağrılmasını istiyorsanız bu arayüzü uygulayın.

```cpp
class IFieldUpdatingCallback : public virtual System::Object
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| virtual [FieldUpdated](./fieldupdated/)(System::SharedPtr\<Aspose::Words::Fields::Field\>) | Bir alan güncellendikten hemen sonra çağrılan kullanıcı tanımlı bir yöntem. |
| virtual [FieldUpdating](./fieldupdating/)(System::SharedPtr\<Aspose::Words::Fields::Field\>) | Bir alan güncellenmeden hemen önce çağrılan kullanıcı tanımlı bir yöntem. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## Ayrıca Bakınız

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
