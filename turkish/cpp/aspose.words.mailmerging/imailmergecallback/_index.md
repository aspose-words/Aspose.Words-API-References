---
title: "Aspose::Words::MailMerging::IMailMergeCallback interface"
linktitle: "IMailMergeCallback"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::MailMerging::IMailMergeCallback arayüzü. C++'ta birleştirme işlemi sırasında bildirim almak istiyorsanız bu arayüzü uygulayın."
type: docs
weight: 8000
url: /tr/cpp/aspose.words.mailmerging/imailmergecallback/
---
## IMailMergeCallback interface


Posta birleştirme gerçekleştirildiği sırada bildirim almak istiyorsanız bu arayüzü uygulayın.

```cpp
class IMailMergeCallback : public virtual System::Object
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [TagsReplaced](./tagsreplaced/)() | Metin etiketleri "mustache" MERGEFIELD alanlarıyla değiştirildiğinde çağrılır. |
| static [Type](./type/)() |  |
## Ayrıca Bakınız

* Namespace [Aspose::Words::MailMerging](../)
* Library [Aspose.Words for C++](../../)
