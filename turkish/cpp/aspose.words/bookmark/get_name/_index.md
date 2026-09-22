---
title: "Aspose::Words::Bookmark::get_Name yöntemi"
linktitle: "get_Name"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Bookmark::get_Name yöntemi. Yer işaretinin adını C++'da alır veya ayarlar."
type: docs
weight: 7000
url: /tr/cpp/aspose.words/bookmark/get_name/
---
## Bookmark::get_Name method


Yer iminin adını alır veya ayarlar.

```cpp
System::String Aspose::Words::Bookmark::get_Name()
```


## Örnekler



Bir yer işareti eklemenin nasıl yapılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Geçerli bir yer işaretinin bir adı, bir BookmarkStart ve bir BookmarkEnd düğümü vardır.
// Yer işaretlerinin adlarındaki boşluklar, kaydedilen belgeyi Microsoft Word ile açarsak alt çizgilere dönüştürülür.
// Microsoft Word'de Ekle -> Bağlantılar -> Yer İşareti yoluyla yer işareti adını vurgular ve "Git" düğmesine basarsak,
// imleç, BookmarkStart ve BookmarkEnd düğümleri arasında bulunan metne atlayacaktır.
builder->StartBookmark(u"My Bookmark");
builder->Write(u"Contents of MyBookmark.");
builder->EndBookmark(u"My Bookmark");

// Yer işaretleri bu koleksiyonda depolanır.
ASSERT_EQ(u"My Bookmark", doc->get_Range()->get_Bookmarks()->idx_get(0)->get_Name());

doc->Save(get_ArtifactsDir() + u"Bookmarks.Insert.docx");
```

## Ayrıca Bakınız

* Class [Bookmark](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
