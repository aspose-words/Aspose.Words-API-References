---
title: "Aspose::Words::DocumentBase::get_Document yöntemi"
linktitle: "get_Document"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::DocumentBase::get_Document yöntemi. Bu örneği C++'ta alır."
type: docs
weight: 3000
url: /tr/cpp/aspose.words/documentbase/get_document/
---
## DocumentBase::get_Document method


Bu örneği alır.

```cpp
System::SharedPtr<Aspose::Words::DocumentBase> Aspose::Words::DocumentBase::get_Document() const override
```


## Örnekler



Basit bir belge nasıl oluşturulacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Yeni Document nesneleri varsayılan olarak minimum düğüm setiyle gelir
// metin ve şekiller gibi içerik eklemeye başlamak için gereken: bir Section, bir Body ve bir Paragraph.
doc->AppendChild<System::SharedPtr<Aspose::Words::Section>>(System::MakeObject<Aspose::Words::Section>(doc))->AppendChild<System::SharedPtr<Aspose::Words::Body>>(System::MakeObject<Aspose::Words::Body>(doc))->AppendChild<System::SharedPtr<Aspose::Words::Paragraph>>(System::MakeObject<Aspose::Words::Paragraph>(doc))->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!"));
```

## Ayrıca Bakınız

* Class [DocumentBase](../)
* Class [DocumentBase](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
