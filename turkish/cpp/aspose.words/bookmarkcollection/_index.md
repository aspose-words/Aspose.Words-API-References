---
title: "Aspose::Words::BookmarkCollection class"
linktitle: "BookmarkCollection"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::BookmarkCollection class. Belirtilen aralıktaki yer imlerini temsil eden Bookmark nesnelerinin bir koleksiyonudur. Daha fazla bilgi için C++ belgeleri makalesini ziyaret edin."
type: docs
weight: 4000
url: /tr/cpp/aspose.words/bookmarkcollection/
---
## BookmarkCollection class


Belirtilen aralıktaki yer imlerini temsil eden bir [Bookmark](../bookmark/) nesneleri koleksiyonu. Daha fazla bilgi için [Working with Bookmarks](https://docs.aspose.com/words/cpp/working-with-bookmarks/) belgeleri makalesini ziyaret edin.

```cpp
class BookmarkCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Bookmark>>
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [Clear](./clear/)() | Bu koleksiyondaki ve belgedeki tüm yer imlerini kaldırır. |
| [get_Count](./get_count/)() | Koleksiyondaki yer imlerinin sayısını döndürür. |
| [GetEnumerator](./getenumerator/)() override | Bir enumeratör nesnesi döndürür. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Belirtilen indeksteki bir yer imini döndürür. |
| [idx_get](./idx_get/)(const System::String\&) | İsme göre bir yer imini döndürür. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)(const System::SharedPtr\<Aspose::Words::Bookmark\>\&) | Belirtilen yer imini belgeden kaldırır. |
| [Remove](./remove/)(const System::String\&) | Belirtilen isimdeki bir yer imini kaldırır. |
| [RemoveAt](./removeat/)(int32_t) | Belirtilen indeksteki bir yer imini kaldırır. |
| static [Type](./type/)() |  |
## Ayrıca Bakınız

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
