---
title: "Aspose::Words::Fonts::FontInfoCollection::Contains yöntemi"
linktitle: "Contains"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fonts::FontInfoCollection::Contains yöntemi. Koleksiyonun verilen ada sahip bir yazı tipini içerip içermediğini C++'ta belirler."
type: docs
weight: 5000
url: /tr/cpp/aspose.words.fonts/fontinfocollection/contains/
---
## FontInfoCollection::Contains method


Koleksiyonun verilen isimde bir yazı tipi içerip içermediğini belirler.

```cpp
bool Aspose::Words::Fonts::FontInfoCollection::Contains(const System::String &name)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| name | const System::String\& | Bulunacak yazı tipinin büyük/küçük harfe duyarsız adı. |

### ReturnValue

**true** if the item is found in the collection; otherwise, **false**.

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
