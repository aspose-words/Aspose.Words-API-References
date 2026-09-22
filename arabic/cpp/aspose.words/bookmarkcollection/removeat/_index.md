---
title: "طريقة Aspose::Words::BookmarkCollection::RemoveAt"
linktitle: "RemoveAt"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::BookmarkCollection::RemoveAt. يزيل إشارة مرجعية عند الفهرس المحدد في C++."
type: docs
weight: 9000
url: /ar/cpp/aspose.words/bookmarkcollection/removeat/
---
## BookmarkCollection::RemoveAt method


يزيل علامة مرجعية في الفهرس المحدد.

```cpp
void Aspose::Words::BookmarkCollection::RemoveAt(int32_t index)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| index | int32_t | الفهرس الصفري للعلامة المرجعية التي سيتم إزالتها. |

## أمثلة



يوضح كيفية إزالة العلامات المرجعية من مستند.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// أدرج خمس علامات مرجعية بنص داخل حدودها.
for (int32_t i = 1; i <= 5; i++)
{
    System::String bookmarkName = System::String(u"MyBookmark_") + i;

    builder->StartBookmark(bookmarkName);
    builder->Write(System::String::Format(u"Text inside {0}.", bookmarkName));
    builder->EndBookmark(bookmarkName);
    builder->InsertBreak(Aspose::Words::BreakType::ParagraphBreak);
}

// هذه المجموعة تخزن العلامات المرجعية.
System::SharedPtr<Aspose::Words::BookmarkCollection> bookmarks = doc->get_Range()->get_Bookmarks();

ASSERT_EQ(5, bookmarks->get_Count());

// هناك عدة طرق لإزالة العلامات المرجعية.
// 1 -  استدعاء طريقة Remove للعلامة المرجعية:
bookmarks->idx_get(u"MyBookmark_1")->Remove();

ASSERT_FALSE(bookmarks->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Bookmark>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Bookmark> b)>>([](System::SharedPtr<Aspose::Words::Bookmark> b) -> bool
{
    return b->get_Name() == u"MyBookmark_1";
}))));

// 2 -  تمرير العلامة المرجعية إلى طريقة Remove للمجموعة:
System::SharedPtr<Aspose::Words::Bookmark> bookmark = doc->get_Range()->get_Bookmarks()->idx_get(0);
doc->get_Range()->get_Bookmarks()->Remove(bookmark);

ASSERT_FALSE(bookmarks->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Bookmark>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Bookmark> b)>>([](System::SharedPtr<Aspose::Words::Bookmark> b) -> bool
{
    return b->get_Name() == u"MyBookmark_2";
}))));

// 3 -  إزالة علامة مرجعية من المجموعة بالاسم:
doc->get_Range()->get_Bookmarks()->Remove(u"MyBookmark_3");

ASSERT_FALSE(bookmarks->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Bookmark>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Bookmark> b)>>([](System::SharedPtr<Aspose::Words::Bookmark> b) -> bool
{
    return b->get_Name() == u"MyBookmark_3";
}))));

// 4 -  إزالة علامة مرجعية عند فهرس في مجموعة العلامات المرجعية:
doc->get_Range()->get_Bookmarks()->RemoveAt(0);

ASSERT_FALSE(bookmarks->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Bookmark>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Bookmark> b)>>([](System::SharedPtr<Aspose::Words::Bookmark> b) -> bool
{
    return b->get_Name() == u"MyBookmark_4";
}))));

// يمكننا مسح مجموعة العلامات المرجعية بالكامل.
bookmarks->Clear();

// النص الذي كان داخل العلامات المرجعية لا يزال موجودًا في المستند.
ASSERT_EQ(0, bookmarks->get_Count());
ASSERT_EQ(System::String(u"Text inside MyBookmark_1.\r") + u"Text inside MyBookmark_2.\r" + u"Text inside MyBookmark_3.\r" + u"Text inside MyBookmark_4.\r" + u"Text inside MyBookmark_5.", doc->GetText().Trim());
```

## انظر أيضًا

* Class [BookmarkCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
