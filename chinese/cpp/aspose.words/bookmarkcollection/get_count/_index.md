---
title: "Aspose::Words::BookmarkCollection::get_Count 方法"
linktitle: "get_Count"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::BookmarkCollection::get_Count 方法。返回集合中书签的数量（C++）。"
type: docs
weight: 3000
url: /zh/cpp/aspose.words/bookmarkcollection/get_count/
---
## BookmarkCollection::get_Count method


返回集合中书签的数量。

```cpp
int32_t Aspose::Words::BookmarkCollection::get_Count()
```


## 示例



展示如何从文档中删除书签。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 在其边界内插入五个带有文本的书签。
for (int32_t i = 1; i <= 5; i++)
{
    System::String bookmarkName = System::String(u"MyBookmark_") + i;

    builder->StartBookmark(bookmarkName);
    builder->Write(System::String::Format(u"Text inside {0}.", bookmarkName));
    builder->EndBookmark(bookmarkName);
    builder->InsertBreak(Aspose::Words::BreakType::ParagraphBreak);
}

// 此集合存储书签。
System::SharedPtr<Aspose::Words::BookmarkCollection> bookmarks = doc->get_Range()->get_Bookmarks();

ASSERT_EQ(5, bookmarks->get_Count());

// 有多种删除书签的方法。
// 1 - 调用书签的 Remove 方法：
bookmarks->idx_get(u"MyBookmark_1")->Remove();

ASSERT_FALSE(bookmarks->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Bookmark>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Bookmark> b)>>([](System::SharedPtr<Aspose::Words::Bookmark> b) -> bool
{
    return b->get_Name() == u"MyBookmark_1";
}))));

// 2 - 将书签传递给集合的 Remove 方法：
System::SharedPtr<Aspose::Words::Bookmark> bookmark = doc->get_Range()->get_Bookmarks()->idx_get(0);
doc->get_Range()->get_Bookmarks()->Remove(bookmark);

ASSERT_FALSE(bookmarks->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Bookmark>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Bookmark> b)>>([](System::SharedPtr<Aspose::Words::Bookmark> b) -> bool
{
    return b->get_Name() == u"MyBookmark_2";
}))));

// 3 - 按名称从集合中删除书签：
doc->get_Range()->get_Bookmarks()->Remove(u"MyBookmark_3");

ASSERT_FALSE(bookmarks->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Bookmark>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Bookmark> b)>>([](System::SharedPtr<Aspose::Words::Bookmark> b) -> bool
{
    return b->get_Name() == u"MyBookmark_3";
}))));

// 4 - 在书签集合中按索引删除书签：
doc->get_Range()->get_Bookmarks()->RemoveAt(0);

ASSERT_FALSE(bookmarks->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Bookmark>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Bookmark> b)>>([](System::SharedPtr<Aspose::Words::Bookmark> b) -> bool
{
    return b->get_Name() == u"MyBookmark_4";
}))));

// 我们可以清除整个书签集合。
bookmarks->Clear();

// 书签内部的文本仍然存在于文档中。
ASSERT_EQ(0, bookmarks->get_Count());
ASSERT_EQ(System::String(u"Text inside MyBookmark_1.\r") + u"Text inside MyBookmark_2.\r" + u"Text inside MyBookmark_3.\r" + u"Text inside MyBookmark_4.\r" + u"Text inside MyBookmark_5.", doc->GetText().Trim());
```

## 另见

* Class [BookmarkCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
