---
title: "Aspose::Words::Document::get_OriginalLoadFormat yöntemi"
linktitle: "get_OriginalLoadFormat"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Document::get_OriginalLoadFormat yöntemi. Bu nesneye yüklü olan orijinal belgenin formatını C++'da alır."
type: docs
weight: 41000
url: /tr/cpp/aspose.words/document/get_originalloadformat/
---
## Document::get_OriginalLoadFormat method


Bu nesneye yüklü olan orijinal belgenin formatını alır.

```cpp
Aspose::Words::LoadFormat Aspose::Words::Document::get_OriginalLoadFormat() const
```

## Açıklamalar


Yeni bir boş belge oluşturduysanız, [Doc](../../loadformat/) değerini döndürür.

## Örnekler



Bir belgenin yükleme işleminin ayrıntılarını nasıl alacağınızı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

ASSERT_EQ(get_MyDir() + u"Document.docx", doc->get_OriginalFileName());
ASSERT_EQ(Aspose::Words::LoadFormat::Docx, doc->get_OriginalLoadFormat());
```

## Ayrıca Bakınız

* Enum [LoadFormat](../../loadformat/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
