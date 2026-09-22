---
title: "Aspose::Words::BookmarkCollection::get_Count metodu"
linktitle: "get_Count"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::BookmarkCollection::get_Count metodu. Koleksiyondaki yer imi sayısını C++'ta döndürür."
type: docs
weight: 3000
url: /tr/cpp/aspose.words/bookmarkcollection/get_count/
---
## BookmarkCollection::get_Count method


Koleksiyondaki yer imlerinin sayısını döndürür.

```cpp
int32_t Aspose::Words::BookmarkCollection::get_Count()
```


## Örnekler



Bir belgeden yer imlerini nasıl kaldıracağınızı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Sınırları içinde metin olan beş yer imi ekleyin.
for (int32_t i = 1; i <= 5; i++)
{
    System::String bookmarkName = System::String(u"MyBookmark_") + i;

    builder->StartBookmark(bookmarkName);
    builder->Write(System::String::Format(u"Text inside {0}.", bookmarkName));
    builder->EndBookmark(bookmarkName);
    builder->InsertBreak(Aspose::Words::BreakType::ParagraphBreak);
}

// Bu koleksiyon yer imlerini depolar.
System::SharedPtr<Aspose::Words::BookmarkCollection> bookmarks = doc->get_Range()->get_Bookmarks();

ASSERT_EQ(5, bookmarks->get_Count());

// Yer imlerini kaldırmanın birkaç yolu vardır.
// 1 -  Yer iminin Remove metodunu çağırma:
bookmarks->idx_get(u"MyBookmark_1")->Remove();

ASSERT_FALSE(bookmarks->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Bookmark>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Bookmark> b)>>([](System::SharedPtr<Aspose::Words::Bookmark> b) -> bool
{
    return b->get_Name() == u"MyBookmark_1";
}))));

// 2 -  Yer imini koleksiyonun Remove metoduna geçirme:
System::SharedPtr<Aspose::Words::Bookmark> bookmark = doc->get_Range()->get_Bookmarks()->idx_get(0);
doc->get_Range()->get_Bookmarks()->Remove(bookmark);

ASSERT_FALSE(bookmarks->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Bookmark>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Bookmark> b)>>([](System::SharedPtr<Aspose::Words::Bookmark> b) -> bool
{
    return b->get_Name() == u"MyBookmark_2";
}))));

// 3 -  Yer imini isimle koleksiyondan kaldırma:
doc->get_Range()->get_Bookmarks()->Remove(u"MyBookmark_3");

ASSERT_FALSE(bookmarks->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Bookmark>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Bookmark> b)>>([](System::SharedPtr<Aspose::Words::Bookmark> b) -> bool
{
    return b->get_Name() == u"MyBookmark_3";
}))));

// 4 -  Yer imi koleksiyonunda bir indekste yer imini kaldırma:
doc->get_Range()->get_Bookmarks()->RemoveAt(0);

ASSERT_FALSE(bookmarks->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Bookmark>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Bookmark> b)>>([](System::SharedPtr<Aspose::Words::Bookmark> b) -> bool
{
    return b->get_Name() == u"MyBookmark_4";
}))));

// Tüm yer imi koleksiyonunu temizleyebiliriz.
bookmarks->Clear();

// Yer imlerinin içinde bulunan metin hâlâ belgede mevcut.
ASSERT_EQ(0, bookmarks->get_Count());
ASSERT_EQ(System::String(u"Text inside MyBookmark_1.\r") + u"Text inside MyBookmark_2.\r" + u"Text inside MyBookmark_3.\r" + u"Text inside MyBookmark_4.\r" + u"Text inside MyBookmark_5.", doc->GetText().Trim());
```

## Ayrıca Bakınız

* Class [BookmarkCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
