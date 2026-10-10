---
title: "Aspose::Words::BookmarkCollection::idx_get 方法"
linktitle: "idx_get"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::BookmarkCollection::idx_get 方法。根据名称返回书签（C++）。"
type: docs
weight: 6000
url: /zh/cpp/aspose.words/bookmarkcollection/idx_get/
---
## BookmarkCollection::idx_get(const System::String\&) method


按名称返回书签。

```cpp
System::SharedPtr<Aspose::Words::Bookmark> Aspose::Words::BookmarkCollection::idx_get(const System::String &bookmarkName)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| bookmarkName | const System::String\& | 书签的大小写不敏感名称。 |
## 备注


如果找不到具有指定名称的书签，则返回 **null**。

## 另见

* Class [Bookmark](../../bookmark/)
* Class [BookmarkCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## BookmarkCollection::idx_get(int32_t) method


返回指定索引处的书签。

```cpp
System::SharedPtr<Aspose::Words::Bookmark> Aspose::Words::BookmarkCollection::idx_get(int32_t index)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| index | int32_t | 集合中的索引。 |
## 备注


索引从零开始。

允许使用负索引，并表示从集合的末尾访问。例如 -1 表示最后一个项目，-2 表示倒数第二个，依此类推。

如果索引大于或等于列表中的项目数，则返回空引用。

如果索引为负且其绝对值大于列表中的项目数，则返回空引用。

## 另见

* Class [Bookmark](../../bookmark/)
* Class [BookmarkCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
