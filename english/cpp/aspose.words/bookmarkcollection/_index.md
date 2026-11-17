---
title: Aspose::Words::BookmarkCollection class
linktitle: BookmarkCollection
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::BookmarkCollection class. A collection of Bookmark objects that represent the bookmarks in the specified range. To learn more, visit the  documentation article in C++.'
type: docs
weight: 4000
url: /cpp/aspose.words/bookmarkcollection/
---
## BookmarkCollection class


A collection of [Bookmark](../bookmark/) objects that represent the bookmarks in the specified range. To learn more, visit the [Working with Bookmarks](https://docs.aspose.com/words/cpp/working-with-bookmarks/) documentation article.

```cpp
class BookmarkCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Bookmark>>
```

## Methods

| Method | Description |
| --- | --- |
| [Clear](./clear/)() | Removes all bookmarks from this collection and from the document. |
| [get_Count](./get_count/)() | Returns the number of bookmarks in the collection. |
| [GetEnumerator](./getenumerator/)() override | Returns an enumerator object. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Returns a bookmark at the specified index. |
| [idx_get](./idx_get/)(const System::String\&) | Returns a bookmark by name. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)(const System::SharedPtr\<Aspose::Words::Bookmark\>\&) | Removes the specified bookmark from the document. |
| [Remove](./remove/)(const System::String\&) | Removes a bookmark with the specified name. |
| [RemoveAt](./removeat/)(int32_t) | Removes a bookmark at the specified index. |
| static [Type](./type/)() |  |
## See Also

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
