---
title: "Aspose::Words::IDocumentMergerPlugin arayüzü"
linktitle: "IDocumentMergerPlugin"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::IDocumentMergerPlugin arabirimi. C++'ta Pdf belgelerini birleştirebilen harici birleştirme eklentisi için bir arabirim tanımlar."
type: docs
weight: 76500
url: /tr/cpp/aspose.words/idocumentmergerplugin/
---
## IDocumentMergerPlugin interface


Pdf belgelerini birleştirebilen harici birleştirici eklentisi için bir arayüz tanımlar.

```cpp
class IDocumentMergerPlugin : public virtual System::Object
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Merge](./merge/)(System::SharedPtr\<System::IO::Stream\>, System::ArrayPtr\<System::SharedPtr\<System::IO::Stream\>\>, System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\>) | Belirtilen giriş ve çıkış akışlarını kullanarak verilen giriş PDF belgelerini tek bir çıkış PDF belgesine birleştirir. |
| static [Type](./type/)() |  |
## Ayrıca Bakınız

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
