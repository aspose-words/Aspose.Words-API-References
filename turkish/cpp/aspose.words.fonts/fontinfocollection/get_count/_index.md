---
title: "Aspose::Words::Fonts::FontInfoCollection::get_Count metodu"
linktitle: "get_Count"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fonts::FontInfoCollection::get_Count metodu. C++'ta koleksiyonda bulunan öğe sayısını alır."
type: docs
weight: 7000
url: /tr/cpp/aspose.words.fonts/fontinfocollection/get_count/
---
## FontInfoCollection::get_Count method


Koleksiyonda bulunan eleman sayısını alır.

```cpp
int32_t Aspose::Words::Fonts::FontInfoCollection::get_Count()
```


## Örnekler



Boş belgede bulunan yazı tipleri hakkında bilgi gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Boş bir belge 3 varsayılan yazı tipi içerir. Belgede her bir yazı tipi
// ilgili FontInfo nesnesine sahip olacak ve bu nesne o yazı tipiyle ilgili ayrıntıları içerir.
ASSERT_EQ(3, doc->get_FontInfos()->get_Count());

ASSERT_TRUE(doc->get_FontInfos()->Contains(u"Times New Roman"));
ASSERT_EQ(204, doc->get_FontInfos()->idx_get(u"Times New Roman")->get_Charset());

ASSERT_TRUE(doc->get_FontInfos()->Contains(u"Symbol"));
ASSERT_TRUE(doc->get_FontInfos()->Contains(u"Arial"));
```

## Ayrıca Bakınız

* Class [FontInfoCollection](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
