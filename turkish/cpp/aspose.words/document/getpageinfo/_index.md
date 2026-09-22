---
title: "Aspose::Words::Document::GetPageInfo metodu"
linktitle: "GetPageInfo"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Document::GetPageInfo metodu. C++'ta bir sayfanın boyutu, yönlendirmesi ve baskı ya da renderlama için faydalı olabilecek diğer bilgileri alır."
type: docs
weight: 62000
url: /tr/cpp/aspose.words/document/getpageinfo/
---
## Document::GetPageInfo method


Sayfa boyutunu, yönünü ve yazdırma veya oluşturma için faydalı olabilecek diğer sayfa bilgilerini alır.

```cpp
System::SharedPtr<Aspose::Words::Rendering::PageInfo> Aspose::Words::Document::GetPageInfo(int32_t pageIndex)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| pageIndex | int32_t | 0 tabanlı sayfa indeksi. |

## Örnekler



Sayfanın renkli olup olmadığını nasıl kontrol edeceğinizi gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

// Belgenin ilk sayfasının renkli olmadığını kontrol edin.
ASSERT_FALSE(doc->GetPageInfo(0)->get_Colored());
```

## Ayrıca Bakınız

* Class [PageInfo](../../../aspose.words.rendering/pageinfo/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
