---
title: "Aspose::Words::MailMerging::IFieldMergingCallback arayüzü"
linktitle: "IFieldMergingCallback"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::MailMerging::IFieldMergingCallback arabirimi. Bu arabirimi, C++'ta bir posta birleştirme işlemi sırasında verilerin birleştirme alanlarına nasıl ekleneceğini kontrol etmek istiyorsanız uygulayın."
type: docs
weight: 7000
url: /tr/cpp/aspose.words.mailmerging/ifieldmergingcallback/
---
## IFieldMergingCallback interface


Bir posta birleştirme işlemi sırasında verilerin birleştirme alanlarına nasıl ekleneceğini kontrol etmek istiyorsanız bu arayüzü uygulayın.

```cpp
class IFieldMergingCallback : public virtual System::Object
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| virtual [FieldMerging](./fieldmerging/)(System::SharedPtr\<Aspose::Words::MailMerging::FieldMergingArgs\>) | Aspose.Words posta birleştirme motoru birleştirme alanına veri eklemek üzereyken çağrılır. |
| [GetType](./gettype/)() const override |  |
| virtual [ImageFieldMerging](./imagefieldmerging/)(System::SharedPtr\<Aspose::Words::MailMerging::ImageFieldMergingArgs\>) | Aspose.Words posta birleştirme motoru birleştirme alanına bir resim eklemek üzereyken çağrılır. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## Ayrıca Bakınız

* Namespace [Aspose::Words::MailMerging](../)
* Library [Aspose.Words for C++](../../)
