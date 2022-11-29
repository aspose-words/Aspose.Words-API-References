---
title: Remove
second_title: Aspose.Words for C++ API Reference
description: Removes the specified bookmark from the document.
type: docs
weight: 53
url: /cpp/aspose.words/bookmarkcollection/remove/
---
## BookmarkCollection::Remove(const System::SharedPtr\<Aspose::Words::Bookmark\>\&) method


Removes the specified bookmark from the document.

```cpp
void Aspose::Words::BookmarkCollection::Remove(const System::SharedPtr<Aspose::Words::Bookmark> &bookmark)
```


| Parameter | Type | Description |
| --- | --- | --- |
| bookmark | const System::SharedPtr\<Aspose::Words::Bookmark\>\& | The bookmark to remove. |

## Examples



Shows how to remove bookmarks from a document. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// Insert five bookmarks with text inside their boundaries.
for (int i = 1; i <= 5; i++)
{
    String bookmarkName = String(u"MyBookmark_") + i;

    builder->StartBookmark(bookmarkName);
    builder->Write(String::Format(u"Text inside {0}.", bookmarkName));
    builder->EndBookmark(bookmarkName);
    builder->InsertBreak(BreakType::ParagraphBreak);
}

// This collection stores bookmarks.
SharedPtr<BookmarkCollection> bookmarks = doc->get_Range()->get_Bookmarks();

ASSERT_EQ(5, bookmarks->get_Count());

// There are several ways of removing bookmarks.
// 1 -  Calling the bookmark's Remove method:
bookmarks->idx_get(u"MyBookmark_1")->Remove();

ASSERT_FALSE(bookmarks->LINQ_Any([](SharedPtr<Bookmark> b) { return b->get_Name() == u"MyBookmark_1"; }));

// 2 -  Passing the bookmark to the collection's Remove method:
SharedPtr<Bookmark> bookmark = doc->get_Range()->get_Bookmarks()->idx_get(0);
doc->get_Range()->get_Bookmarks()->Remove(bookmark);

ASSERT_FALSE(bookmarks->LINQ_Any([](SharedPtr<Bookmark> b) { return b->get_Name() == u"MyBookmark_2"; }));

// 3 -  Removing a bookmark from the collection by name:
doc->get_Range()->get_Bookmarks()->Remove(u"MyBookmark_3");

ASSERT_FALSE(bookmarks->LINQ_Any([](SharedPtr<Bookmark> b) { return b->get_Name() == u"MyBookmark_3"; }));

// 4 -  Removing a bookmark at an index in the bookmark collection:
doc->get_Range()->get_Bookmarks()->RemoveAt(0);

ASSERT_FALSE(bookmarks->LINQ_Any([](SharedPtr<Bookmark> b) { return b->get_Name() == u"MyBookmark_4"; }));

// We can clear the entire bookmark collection.
bookmarks->Clear();

// The text that was inside the bookmarks is still present in the document.
ASSERT_EQ(0, bookmarks->get_Count());
ASSERT_EQ(String(u"Text inside MyBookmark_1.\r") + u"Text inside MyBookmark_2.\r" + u"Text inside MyBookmark_3.\r" + u"Text inside MyBookmark_4.\r" +
              u"Text inside MyBookmark_5.",
          doc->GetText().Trim());
```

## See Also

* Class [Bookmark](../../bookmark/)
* Class [BookmarkCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words](../../../)
## BookmarkCollection::Remove(const System::String\&) method


Removes a bookmark with the specified name.

```cpp
void Aspose::Words::BookmarkCollection::Remove(const System::String &bookmarkName)
```


| Parameter | Type | Description |
| --- | --- | --- |
| bookmarkName | const System::String\& | The case-insensitive name of the bookmark to remove. |

## Examples



Shows how to remove bookmarks from a document. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// Insert five bookmarks with text inside their boundaries.
for (int i = 1; i <= 5; i++)
{
    String bookmarkName = String(u"MyBookmark_") + i;

    builder->StartBookmark(bookmarkName);
    builder->Write(String::Format(u"Text inside {0}.", bookmarkName));
    builder->EndBookmark(bookmarkName);
    builder->InsertBreak(BreakType::ParagraphBreak);
}

// This collection stores bookmarks.
SharedPtr<BookmarkCollection> bookmarks = doc->get_Range()->get_Bookmarks();

ASSERT_EQ(5, bookmarks->get_Count());

// There are several ways of removing bookmarks.
// 1 -  Calling the bookmark's Remove method:
bookmarks->idx_get(u"MyBookmark_1")->Remove();

ASSERT_FALSE(bookmarks->LINQ_Any([](SharedPtr<Bookmark> b) { return b->get_Name() == u"MyBookmark_1"; }));

// 2 -  Passing the bookmark to the collection's Remove method:
SharedPtr<Bookmark> bookmark = doc->get_Range()->get_Bookmarks()->idx_get(0);
doc->get_Range()->get_Bookmarks()->Remove(bookmark);

ASSERT_FALSE(bookmarks->LINQ_Any([](SharedPtr<Bookmark> b) { return b->get_Name() == u"MyBookmark_2"; }));

// 3 -  Removing a bookmark from the collection by name:
doc->get_Range()->get_Bookmarks()->Remove(u"MyBookmark_3");

ASSERT_FALSE(bookmarks->LINQ_Any([](SharedPtr<Bookmark> b) { return b->get_Name() == u"MyBookmark_3"; }));

// 4 -  Removing a bookmark at an index in the bookmark collection:
doc->get_Range()->get_Bookmarks()->RemoveAt(0);

ASSERT_FALSE(bookmarks->LINQ_Any([](SharedPtr<Bookmark> b) { return b->get_Name() == u"MyBookmark_4"; }));

// We can clear the entire bookmark collection.
bookmarks->Clear();

// The text that was inside the bookmarks is still present in the document.
ASSERT_EQ(0, bookmarks->get_Count());
ASSERT_EQ(String(u"Text inside MyBookmark_1.\r") + u"Text inside MyBookmark_2.\r" + u"Text inside MyBookmark_3.\r" + u"Text inside MyBookmark_4.\r" +
              u"Text inside MyBookmark_5.",
          doc->GetText().Trim());
```

## See Also

* Class [BookmarkCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words](../../../)
