---
title: Clear
second_title: Aspose.Words for C++ API Reference
description: Removes all bookmarks from this collection and from the document.
type: docs
weight: 14
url: /cpp/aspose.words/bookmarkcollection/clear/
---
## BookmarkCollection::Clear method


Removes all bookmarks from this collection and from the document.

```cpp
void Aspose::Words::BookmarkCollection::Clear()
```


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
