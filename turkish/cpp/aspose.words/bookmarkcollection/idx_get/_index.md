---
title: "Aspose::Words::BookmarkCollection::idx_get metodu"
linktitle: "idx_get"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::BookmarkCollection::idx_get metodu. C++'ta bir yer imini isimle döndürür."
type: docs
weight: 6000
url: /tr/cpp/aspose.words/bookmarkcollection/idx_get/
---
## BookmarkCollection::idx_get(const System::String\&) method


İsme göre bir yer imini döndürür.

```cpp
System::SharedPtr<Aspose::Words::Bookmark> Aspose::Words::BookmarkCollection::idx_get(const System::String &bookmarkName)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| bookmarkName | const System::String\& | Yer iminin büyük/küçük harfe duyarsız adı. |
## Açıklamalar


Belirtilen isimdeki yer imi bulunamazsa **null** döndürür.

## Ayrıca Bakınız

* Class [Bookmark](../../bookmark/)
* Class [BookmarkCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## BookmarkCollection::idx_get(int32_t) method


Belirtilen indeksteki bir yer imini döndürür.

```cpp
System::SharedPtr<Aspose::Words::Bookmark> Aspose::Words::BookmarkCollection::idx_get(int32_t index)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| index | int32_t | Koleksiyona bir indeks. |
## Açıklamalar


İndeks sıfır tabanlıdır.

Negatif indekslere izin verilir ve koleksiyonun sonundan erişimi gösterir. Örneğin -1 son öğeyi, -2 sondan bir önceki öğeyi vb. ifade eder.

İndeks listedeki öğe sayısına eşit veya daha büyükse, bu null referans döndürür.

İndeks negatif ve mutlak değeri listedeki öğe sayısından büyükse, bu null referans döndürür.

## Ayrıca Bakınız

* Class [Bookmark](../../bookmark/)
* Class [BookmarkCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
