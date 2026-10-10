---
title: "Aspose::Words::Bookmark 类"
linktitle: "书签"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Bookmark 类。表示单个书签。要了解更多，请访问 C++ 文档文章。"
type: docs
weight: 3000
url: /zh/cpp/aspose.words/bookmark/
---
## Bookmark class


表示单个书签。欲了解更多，请访问[书签使用指南](https://docs.aspose.com/words/cpp/working-with-bookmarks/)文档文章。

```cpp
class Bookmark : public System::Object
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [get_BookmarkEnd](./get_bookmarkend/)() | 获取表示书签结束的节点。 |
| [get_BookmarkStart](./get_bookmarkstart/)() const | 获取表示书签开始的节点。 |
| [get_FirstColumn](./get_firstcolumn/)() | 获取与书签关联的表列范围的第一列的零基索引。 |
| [get_IsColumn](./get_iscolumn/)() | 如果此书签是表列书签，则返回 **true**。 |
| [get_LastColumn](./get_lastcolumn/)() | 获取与书签关联的表列范围的最后一列的零基索引。 |
| [get_Name](./get_name/)() | 获取或设置书签的名称。 |
| [get_Text](./get_text/)() | 获取书签中包含的文本。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)() | 从文档中移除书签。不会删除书签内的文本。 |
| [set_Name](./set_name/)(const System::String\&) | 用于设置 [Aspose::Words::Bookmark::get_Name](./get_name/) 的 setter。 |
| [set_Text](./set_text/)(const System::String\&) | 设置书签中包含的文本。 |
| static [Type](./type/)() |  |
## 备注


[Bookmark](./) is a "facade" object that encapsulates two nodes [BookmarkStart](./get_bookmarkstart/) and [BookmarkEnd](./get_bookmarkend/) in a document tree and allows to work with a bookmark as a single object. 
## 另见

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
