---
title: "Aspose::Words::BookmarkCollection 类"
linktitle: "BookmarkCollection"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::BookmarkCollection 类。一个 Bookmark 对象的集合，表示指定范围内的书签。欲了解更多，请访问 C++ 文档文章。"
type: docs
weight: 4000
url: /zh/cpp/aspose.words/bookmarkcollection/
---
## BookmarkCollection class


一个 [Bookmark](../bookmark/) 对象的集合，表示指定范围内的书签。欲了解更多，请访问 [Working with Bookmarks](https://docs.aspose.com/words/cpp/working-with-bookmarks/) 文档文章。

```cpp
class BookmarkCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Bookmark>>
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [Clear](./clear/)() | 从此集合和文档中移除所有书签。 |
| [get_Count](./get_count/)() | 返回集合中书签的数量。 |
| [GetEnumerator](./getenumerator/)() override | 返回一个枚举器对象。 |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | 返回指定索引处的书签。 |
| [idx_get](./idx_get/)(const System::String\&) | 按名称返回书签。 |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)(const System::SharedPtr\<Aspose::Words::Bookmark\>\&) | 从文档中移除指定的书签。 |
| [Remove](./remove/)(const System::String\&) | 移除具有指定名称的书签。 |
| [RemoveAt](./removeat/)(int32_t) | 移除指定索引处的书签。 |
| static [Type](./type/)() |  |
## 另见

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
