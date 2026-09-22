---
title: "Aspose::Words::IRevisionCriteria interface"
linktitle: "IRevisionCriteria"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::IRevisionCriteria interface. Bu arayüzü, belirli bir Revision'ın Accept()/Reject() yöntemleriyle C++'ta kabul edilip reddedileceğini kontrol etmek istiyorsanız uygulayın."
type: docs
weight: 79500
url: /tr/cpp/aspose.words/irevisioncriteria/
---
## IRevisionCriteria interface


Bu arayüzü, belirli bir [Revision](../revision/) öğesinin [Accept()](../)/[Reject()](../) yöntemleriyle kabul edilip reddedileceğini kontrol etmek istiyorsanız uygulayın.

```cpp
class IRevisionCriteria : public virtual System::Object
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [IsMatch](./ismatch/)(System::SharedPtr\<Aspose::Words::Revision\>) | Belirtilen *revision*'ın kriterlere uyup uymadığını kontrol eder. |
| static [Type](./type/)() |  |
## Ayrıca Bakınız

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
