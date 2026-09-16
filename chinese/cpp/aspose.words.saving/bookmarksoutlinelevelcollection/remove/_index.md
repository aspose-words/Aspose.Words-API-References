---
title: "Aspose::Words::Saving::BookmarksOutlineLevelCollection::Remove 方法"
linktitle: "Remove"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::BookmarksOutlineLevelCollection::Remove 方法。删除集合中具有指定名称的书签（在 C++ 中）。"
type: docs
weight: 17000
url: /zh/cpp/aspose.words.saving/bookmarksoutlinelevelcollection/remove/
---
## BookmarksOutlineLevelCollection::Remove method


从集合中移除具有指定名称的书签。

```cpp
void Aspose::Words::Saving::BookmarksOutlineLevelCollection::Remove(const System::String &name)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| name | const System::String\& | 书签的大小写不敏感名称。 |

## 示例



展示如何为书签设置大纲级别。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 插入一个书签，并在其内部嵌套另一个书签。
builder->StartBookmark(u"Bookmark 1");
builder->Writeln(u"Text inside Bookmark 1.");

builder->StartBookmark(u"Bookmark 2");
builder->Writeln(u"Text inside Bookmark 1 and 2.");
builder->EndBookmark(u"Bookmark 2");

builder->Writeln(u"Text inside Bookmark 1.");
builder->EndBookmark(u"Bookmark 1");

// 插入另一个书签。
builder->StartBookmark(u"Bookmark 3");
builder->Writeln(u"Text inside Bookmark 3.");
builder->EndBookmark(u"Bookmark 3");

// 保存为 .pdf 时，书签可以通过下拉菜单访问，并被大多数阅读器用作锚点。
// 书签也可以拥有数值的大纲级别，
// 使得在阅读器中折叠时，低级别的大纲条目可以隐藏高级别的子条目。
auto pdfSaveOptions = System::MakeObject<Aspose::Words::Saving::PdfSaveOptions>();
System::SharedPtr<Aspose::Words::Saving::BookmarksOutlineLevelCollection> outlineLevels = pdfSaveOptions->get_OutlineOptions()->get_BookmarksOutlineLevels();

outlineLevels->Add(u"Bookmark 1", 1);
outlineLevels->Add(u"Bookmark 2", 2);
outlineLevels->Add(u"Bookmark 3", 3);

ASSERT_EQ(3, outlineLevels->get_Count());
ASSERT_TRUE(outlineLevels->Contains(u"Bookmark 1"));
ASSERT_EQ(1, outlineLevels->idx_get(0));
ASSERT_EQ(2, outlineLevels->idx_get(u"Bookmark 2"));
ASSERT_EQ(2, outlineLevels->IndexOfKey(u"Bookmark 3"));

// 我们可以移除两个元素，只留下 "Bookmark 1" 的大纲级别指定。
outlineLevels->RemoveAt(2);
outlineLevels->Remove(u"Bookmark 2");

// 共有九个大纲级别。它们的编号将在保存操作期间进行优化。
// 在这种情况下，级别 "5" 和 "9" 将变为 "2" 和 "3"。
outlineLevels->Add(u"Bookmark 2", 5);
outlineLevels->Add(u"Bookmark 3", 9);

doc->Save(get_ArtifactsDir() + u"BookmarksOutlineLevelCollection.BookmarkLevels.pdf", pdfSaveOptions);

// 清空此集合将保留书签，并将它们全部放在同一大纲级别上。
outlineLevels->Clear();
```

## 另见

* Class [BookmarksOutlineLevelCollection](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
