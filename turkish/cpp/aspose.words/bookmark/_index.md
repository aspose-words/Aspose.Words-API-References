---
title: "Aspose::Words::Bookmark sınıfı"
linktitle: "Yer imi"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Bookmark sınıfı. Tek bir yer imini temsil eder. Daha fazla bilgi edinmek için C++'daki belge makalesini ziyaret edin."
type: docs
weight: 3000
url: /tr/cpp/aspose.words/bookmark/
---
## Bookmark class


Tek bir yer imini temsil eder. Daha fazla bilgi için, [Working with Bookmarks](https://docs.aspose.com/words/cpp/working-with-bookmarks/) dokümantasyon makalesini ziyaret edin.

```cpp
class Bookmark : public System::Object
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [get_BookmarkEnd](./get_bookmarkend/)() | Yer iminin sonunu temsil eden düğümü alır. |
| [get_BookmarkStart](./get_bookmarkstart/)() const | Yer iminin başlangıcını temsil eden düğümü alır. |
| [get_FirstColumn](./get_firstcolumn/)() | Yer imiyle ilişkili tablo sütun aralığının ilk sütununun sıfır tabanlı indeksini alır. |
| [get_IsColumn](./get_iscolumn/)() | Bu yer imi bir tablo sütun yer imi ise **true** döndürür. |
| [get_LastColumn](./get_lastcolumn/)() | Yer imiyle ilişkili tablo sütun aralığının son sütununun sıfır tabanlı indeksini alır. |
| [get_Name](./get_name/)() | Yer iminin adını alır veya ayarlar. |
| [get_Text](./get_text/)() | Yer imi içinde kapsanan metni alır. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)() | Yer imini belgeden kaldırır. Yer imi içindeki metni kaldırmaz. |
| [set_Name](./set_name/)(const System::String\&) | Ayarlayıcı: [Aspose::Words::Bookmark::get_Name](./get_name/). |
| [set_Text](./set_text/)(const System::String\&) | Yer imi içinde kapsanan metni ayarlar. |
| static [Type](./type/)() |  |
## Açıklamalar


[Bookmark](./) is a "facade" object that encapsulates two nodes [BookmarkStart](./get_bookmarkstart/) and [BookmarkEnd](./get_bookmarkend/) in a document tree and allows to work with a bookmark as a single object. 
## Ayrıca Bakınız

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
