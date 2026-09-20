---
title: "Aspose::Words::Saving::BookmarksOutlineLevelCollection 类"
linktitle: "BookmarksOutlineLevelCollection"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::BookmarksOutlineLevelCollection 类。一个包含各个书签大纲级别的集合。要了解更多信息，请访问 C++ 文档文章。"
type: docs
weight: 1000
url: /zh/cpp/aspose.words.saving/bookmarksoutlinelevelcollection/
---
## BookmarksOutlineLevelCollection class


单个书签的大纲级别集合。欲了解更多信息，请访问 [Working with Bookmarks](https://docs.aspose.com/words/cpp/working-with-bookmarks/) 文档文章。

```cpp
class BookmarksOutlineLevelCollection : public System::Collections::Generic::IEnumerable<System::Collections::Generic::KeyValuePair<System::String, int32_t>>
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [Add](./add/)(const System::String\&, int32_t) | 向集合中添加书签。 |
| [begin](./begin/)() |  |
| [begin](./begin/)() const |  |
| [BookmarksOutlineLevelCollection](./bookmarksoutlinelevelcollection/)() |  |
| [cbegin](./cbegin/)() const |  |
| [cend](./cend/)() const |  |
| [Clear](./clear/)() | 从集合中移除所有元素。 |
| [Contains](./contains/)(const System::String\&) | 确定集合是否包含具有给定名称的书签。 |
| [end](./end/)() |  |
| [end](./end/)() const |  |
| [get_Count](./get_count/)() | 获取集合中包含的元素数量。 |
| [GetEnumerator](./getenumerator/)() override | 返回一个可用于遍历集合中所有项的枚举器对象。 |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(const System::String\&) | 获取或设置书签的大纲级别（通过书签名称）。 |
| [idx_get](./idx_get/)(int32_t) | 获取或设置指定索引处的书签大纲级别。 |
| [idx_set](./idx_set/)(const System::String\&, int32_t) | 获取或设置书签的大纲级别（通过书签名称）。 |
| [idx_set](./idx_set/)(int32_t, int32_t) | 获取或设置指定索引处的书签大纲级别。 |
| [IndexOfKey](./indexofkey/)(const System::String\&) | 返回集合中指定书签的零基索引。 |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)(const System::String\&) | 从集合中移除具有指定名称的书签。 |
| [RemoveAt](./removeat/)(int32_t) | 移除指定索引处的书签。 |
| static [Type](./type/)() |  |
| [virtualizeBeginConstIterator](./virtualizebeginconstiterator/)() const override |  |
| [virtualizeBeginIterator](./virtualizebeginiterator/)() override |  |
| [virtualizeEndConstIterator](./virtualizeendconstiterator/)() const override |  |
| [virtualizeEndIterator](./virtualizeenditerator/)() override |  |
## Typedefs

| 类型定义 | 描述 |
| --- | --- |
| [const_iterator](./const_iterator/) |  |
| [iterator](./iterator/) |  |
| [iterator_holder_type](./iterator_holder_type/) |  |
| [virtualized_iterator](./virtualized_iterator/) |  |
| [virtualized_iterator_element](./virtualized_iterator_element/) |  |
## 备注


键是不区分大小写的字符串书签名称。值是整数书签大纲级别。

[Bookmark](../../aspose.words/bookmark/) outline level may be a value from 0 to 9. Specify 0 and Word bookmark will not be displayed in the document outline. Specify 1 and Word bookmark will be displayed in the document outline at level 1; 2 for level 2 and so on.

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

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
