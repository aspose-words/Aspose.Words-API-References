---
title: "Aspose::Words::BookmarkCollection::Remove méthode"
linktitle: "Supprimer"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::BookmarkCollection::Remove méthode. Supprime le signet spécifié du document en C++."
type: docs
weight: 8000
url: /fr/cpp/aspose.words/bookmarkcollection/remove/
---
## BookmarkCollection::Remove(const System::SharedPtr\<Aspose::Words::Bookmark\>\&) method


Supprime le signet spécifié du document.

```cpp
void Aspose::Words::BookmarkCollection::Remove(const System::SharedPtr<Aspose::Words::Bookmark> &bookmark)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| signet | const System::SharedPtr\<Aspose::Words::Bookmark\>\& | Le signet à supprimer. |

## Exemples



Montre comment supprimer des signets d'un document.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Insérez cinq signets avec du texte à l'intérieur de leurs limites.
for (int32_t i = 1; i <= 5; i++)
{
    System::String bookmarkName = System::String(u"MyBookmark_") + i;

    builder->StartBookmark(bookmarkName);
    builder->Write(System::String::Format(u"Text inside {0}.", bookmarkName));
    builder->EndBookmark(bookmarkName);
    builder->InsertBreak(Aspose::Words::BreakType::ParagraphBreak);
}

// Cette collection stocke des signets.
System::SharedPtr<Aspose::Words::BookmarkCollection> bookmarks = doc->get_Range()->get_Bookmarks();

ASSERT_EQ(5, bookmarks->get_Count());

// Il existe plusieurs façons de supprimer des signets.
// 1 -  Appeler la méthode Remove du signet :
bookmarks->idx_get(u"MyBookmark_1")->Remove();

ASSERT_FALSE(bookmarks->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Bookmark>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Bookmark> b)>>([](System::SharedPtr<Aspose::Words::Bookmark> b) -> bool
{
    return b->get_Name() == u"MyBookmark_1";
}))));

// 2 -  Passer le signet à la méthode Remove de la collection :
System::SharedPtr<Aspose::Words::Bookmark> bookmark = doc->get_Range()->get_Bookmarks()->idx_get(0);
doc->get_Range()->get_Bookmarks()->Remove(bookmark);

ASSERT_FALSE(bookmarks->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Bookmark>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Bookmark> b)>>([](System::SharedPtr<Aspose::Words::Bookmark> b) -> bool
{
    return b->get_Name() == u"MyBookmark_2";
}))));

// 3 -  Supprimer un signet de la collection par son nom :
doc->get_Range()->get_Bookmarks()->Remove(u"MyBookmark_3");

ASSERT_FALSE(bookmarks->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Bookmark>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Bookmark> b)>>([](System::SharedPtr<Aspose::Words::Bookmark> b) -> bool
{
    return b->get_Name() == u"MyBookmark_3";
}))));

// 4 -  Supprimer un signet à un index dans la collection de signets :
doc->get_Range()->get_Bookmarks()->RemoveAt(0);

ASSERT_FALSE(bookmarks->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Bookmark>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Bookmark> b)>>([](System::SharedPtr<Aspose::Words::Bookmark> b) -> bool
{
    return b->get_Name() == u"MyBookmark_4";
}))));

// Nous pouvons vider toute la collection de signets.
bookmarks->Clear();

// Le texte qui était à l'intérieur des signets est toujours présent dans le document.
ASSERT_EQ(0, bookmarks->get_Count());
ASSERT_EQ(System::String(u"Text inside MyBookmark_1.\r") + u"Text inside MyBookmark_2.\r" + u"Text inside MyBookmark_3.\r" + u"Text inside MyBookmark_4.\r" + u"Text inside MyBookmark_5.", doc->GetText().Trim());
```

## Voir aussi

* Class [Bookmark](../../bookmark/)
* Class [BookmarkCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## BookmarkCollection::Remove(const System::String\&) method


Supprime un signet avec le nom spécifié.

```cpp
void Aspose::Words::BookmarkCollection::Remove(const System::String &bookmarkName)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| bookmarkName | const System::String\& | Le nom du signet à supprimer, insensible à la casse. |

## Exemples



Montre comment supprimer des signets d'un document.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Insérez cinq signets avec du texte à l'intérieur de leurs limites.
for (int32_t i = 1; i <= 5; i++)
{
    System::String bookmarkName = System::String(u"MyBookmark_") + i;

    builder->StartBookmark(bookmarkName);
    builder->Write(System::String::Format(u"Text inside {0}.", bookmarkName));
    builder->EndBookmark(bookmarkName);
    builder->InsertBreak(Aspose::Words::BreakType::ParagraphBreak);
}

// Cette collection stocke des signets.
System::SharedPtr<Aspose::Words::BookmarkCollection> bookmarks = doc->get_Range()->get_Bookmarks();

ASSERT_EQ(5, bookmarks->get_Count());

// Il existe plusieurs façons de supprimer des signets.
// 1 -  Appeler la méthode Remove du signet :
bookmarks->idx_get(u"MyBookmark_1")->Remove();

ASSERT_FALSE(bookmarks->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Bookmark>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Bookmark> b)>>([](System::SharedPtr<Aspose::Words::Bookmark> b) -> bool
{
    return b->get_Name() == u"MyBookmark_1";
}))));

// 2 -  Passer le signet à la méthode Remove de la collection :
System::SharedPtr<Aspose::Words::Bookmark> bookmark = doc->get_Range()->get_Bookmarks()->idx_get(0);
doc->get_Range()->get_Bookmarks()->Remove(bookmark);

ASSERT_FALSE(bookmarks->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Bookmark>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Bookmark> b)>>([](System::SharedPtr<Aspose::Words::Bookmark> b) -> bool
{
    return b->get_Name() == u"MyBookmark_2";
}))));

// 3 -  Supprimer un signet de la collection par son nom :
doc->get_Range()->get_Bookmarks()->Remove(u"MyBookmark_3");

ASSERT_FALSE(bookmarks->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Bookmark>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Bookmark> b)>>([](System::SharedPtr<Aspose::Words::Bookmark> b) -> bool
{
    return b->get_Name() == u"MyBookmark_3";
}))));

// 4 -  Supprimer un signet à un index dans la collection de signets :
doc->get_Range()->get_Bookmarks()->RemoveAt(0);

ASSERT_FALSE(bookmarks->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Bookmark>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Bookmark> b)>>([](System::SharedPtr<Aspose::Words::Bookmark> b) -> bool
{
    return b->get_Name() == u"MyBookmark_4";
}))));

// Nous pouvons vider toute la collection de signets.
bookmarks->Clear();

// Le texte qui était à l'intérieur des signets est toujours présent dans le document.
ASSERT_EQ(0, bookmarks->get_Count());
ASSERT_EQ(System::String(u"Text inside MyBookmark_1.\r") + u"Text inside MyBookmark_2.\r" + u"Text inside MyBookmark_3.\r" + u"Text inside MyBookmark_4.\r" + u"Text inside MyBookmark_5.", doc->GetText().Trim());
```

## Voir aussi

* Class [BookmarkCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
