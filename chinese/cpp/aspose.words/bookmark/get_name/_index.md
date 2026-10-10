---
title: "Aspose::Words::Bookmark::get_Name 方法"
linktitle: "get_Name"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Bookmark::get_Name 方法。获取或设置书签的名称（C++）。"
type: docs
weight: 7000
url: /zh/cpp/aspose.words/bookmark/get_name/
---
## Bookmark::get_Name method


获取或设置书签的名称。

```cpp
System::String Aspose::Words::Bookmark::get_Name()
```


## 示例



展示如何插入书签。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 有效的书签具有名称、BookmarkStart 和 BookmarkEnd 节点。
// 如果我们使用 Microsoft Word 打开已保存的文档，书签名称中的任何空白字符将被转换为下划线。
// 如果我们在 Microsoft Word 中通过 Insert -> Links -> Bookmark 高亮书签名称，并按下 "Go To" 键，
// 光标将跳转到 BookmarkStart 和 BookmarkEnd 节点之间包含的文本。
builder->StartBookmark(u"My Bookmark");
builder->Write(u"Contents of MyBookmark.");
builder->EndBookmark(u"My Bookmark");

// 书签存储在此集合中。
ASSERT_EQ(u"My Bookmark", doc->get_Range()->get_Bookmarks()->idx_get(0)->get_Name());

doc->Save(get_ArtifactsDir() + u"Bookmarks.Insert.docx");
```

## 另见

* Class [Bookmark](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
