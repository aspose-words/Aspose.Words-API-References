---
title: "Aspose::Words::Fields::IFieldUserPromptRespondent interface"
linktitle: "IFieldUserPromptRespondent"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fields::IFieldUserPromptRespondent arayüzü. C++'ta alan güncellemesi sırasında kullanıcı istemlerine yanıt veren kişiyi temsil eder."
type: docs
weight: 125000
url: /tr/cpp/aspose.words.fields/ifielduserpromptrespondent/
---
## IFieldUserPromptRespondent interface


Alan güncellemesi sırasında kullanıcı istemlerine yanıt veren kişiyi temsil eder.

```cpp
class IFieldUserPromptRespondent : public virtual System::Object
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Respond](./respond/)(System::String, System::String) | Uygulandığında, istem üzerine kullanıcıdan bir yanıt döndürür. Uygulamanız, kullanıcının isteğe yanıt vermediğini göstermek için **null** döndürmelidir (yani kullanıcı istem penceresinde İptal düğmesine basmıştır). |
| static [Type](./type/)() |  |
## Ayrıca Bakınız

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
