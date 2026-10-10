---
title: "Aspose::Words::Document::get_PageCount yöntemi"
linktitle: "get_PageCount"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Document::get_PageCount yöntemi. C++'da en son sayfa yerleşim işlemi tarafından hesaplanan belge içindeki sayfa sayısını alır."
type: docs
weight: 43000
url: /tr/cpp/aspose.words/document/get_pagecount/
---
## Document::get_PageCount method


En son sayfa yerleşim işlemi tarafından hesaplanan belge sayfası sayısını alır.

```cpp
int32_t Aspose::Words::Document::get_PageCount()
```


## Örnekler



Belgedeki sayfa sayısını nasıl sayacağınızı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Page 1");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Write(u"Page 2");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Write(u"Page 3");

// Belgenin beklenen sayfa sayısını doğrulayın.
ASSERT_EQ(3, doc->get_PageCount());

// PageCount özelliğini almak, değeri hesaplamak için belgenin sayfa yerleşimini tetikler.
// Bu işlem, belgeyi sabit sayfa kaydetme formatına render ederken tekrar yapılmak zorunda kalmayacaktır,
// örneğin .pdf. Böylece özellikle daha karmaşık belgelerde zaman kazanabilirsiniz.
doc->Save(get_ArtifactsDir() + u"Document.GetPageCount.pdf");
```

## Ayrıca Bakınız

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
