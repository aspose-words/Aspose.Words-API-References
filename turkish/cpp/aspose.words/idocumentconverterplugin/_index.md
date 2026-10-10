---
title: "Aspose::Words::IDocumentConverterPlugin arayüzü"
linktitle: "IDocumentConverterPlugin"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::IDocumentConverterPlugin arayüzü. C++'ta harici dönüştürücü eklentisi için bir arayüz tanımlar."
type: docs
weight: 76250
url: /tr/cpp/aspose.words/idocumentconverterplugin/
---
## IDocumentConverterPlugin interface


Harici dönüştürücü eklentisi için bir arayüz tanımlar.

```cpp
class IDocumentConverterPlugin : public virtual System::Object
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| virtual [Convert](./convert/)(System::SharedPtr\<System::IO::Stream\>, System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>, System::SharedPtr\<System::IO::Stream\>, System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>) | Belgeyi belirtilen giriş çıkış akışları ve kaydetme seçenekleri kullanarak dönüştürür. |
| virtual [ConvertToImages](./converttoimages/)(System::SharedPtr\<System::IO::Stream\>, System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>, System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>) | Belgeden sayfaları giriş akışından görüntü dizisine dönüştürür. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## Ayrıca Bakınız

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
