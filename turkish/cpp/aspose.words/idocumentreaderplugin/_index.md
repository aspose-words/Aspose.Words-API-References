---
title: "Aspose::Words::IDocumentReaderPlugin arabirimi"
linktitle: "IDocumentReaderPlugin"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::IDocumentReaderPlugin arabirimi. C++'ta bir dosyayı belgeye okuyabilen harici okuyucu eklentileri için bir arabirim tanımlar."
type: docs
weight: 77000
url: /tr/cpp/aspose.words/idocumentreaderplugin/
---
## IDocumentReaderPlugin interface


Bir dosyayı belgeye okuyabilen harici okuyucu eklentileri için bir arayüz tanımlar.

```cpp
class IDocumentReaderPlugin : public virtual System::Object
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Read](./read/)(System::SharedPtr\<System::IO::Stream\>, System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>, System::SharedPtr\<Aspose::Words::Document\>) | Belirtilen akıştan verileri [Document](../document/) örneğine okur. |
| static [Type](./type/)() |  |
## Ayrıca Bakınız

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
