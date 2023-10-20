---
title: BookmarksOutlineLevelCollection Class
linktitle: BookmarksOutlineLevelCollection
articleTitle: BookmarksOutlineLevelCollection
second_title: 用于 .NET 的 Aspose.Words
description: Aspose.Words.Saving.BookmarksOutlineLevelCollection 班级. 单个书签大纲级别的集合 在 C#.
type: docs
weight: 4850
url: /zh/net/aspose.words.saving/bookmarksoutlinelevelcollection/
---
## BookmarksOutlineLevelCollection class

单个书签大纲级别的集合。

```csharp
public class BookmarksOutlineLevelCollection : IEnumerable<KeyValuePair<string, int>>
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [BookmarksOutlineLevelCollection](bookmarksoutlinelevelcollection/)() | 默认构造函数。 |

## 特性

| 姓名 | 描述 |
| --- | --- |
| [Count](../../aspose.words.saving/bookmarksoutlinelevelcollection/count/) { get; } | 获取集合中包含的元素数。 |
| [Item](../../aspose.words.saving/bookmarksoutlinelevelcollection/item/) { get; set; } | 通过书签名称获取或设置书签大纲级别。 (2 indexers) |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [Add](../../aspose.words.saving/bookmarksoutlinelevelcollection/add/)(*string, int*) | 为收藏添加书签。 |
| [Clear](../../aspose.words.saving/bookmarksoutlinelevelcollection/clear/)() | 从集合中删除所有元素。 |
| [Contains](../../aspose.words.saving/bookmarksoutlinelevelcollection/contains/)(*string*) | 确定集合是否包含具有给定名称的书签。 |
| [GetEnumerator](../../aspose.words.saving/bookmarksoutlinelevelcollection/getenumerator/)() |  |
| [IndexOfKey](../../aspose.words.saving/bookmarksoutlinelevelcollection/indexofkey/)(*string*) | 返回集合中指定书签的从零开始的索引。 |
| [Remove](../../aspose.words.saving/bookmarksoutlinelevelcollection/remove/)(*string*) | 从集合中删除具有指定名称的书签。 |
| [RemoveAt](../../aspose.words.saving/bookmarksoutlinelevelcollection/removeat/)(*int*) | 删除指定索引处的书签。 |

## 评论

Key 是不区分大小写的字符串书签名称。值是一个 int 书签大纲级别。

书签大纲级别可以是 0 到 9 之间的值。指定 0，Word 书签将不会显示在文档大纲中。 指定 1，Word 书签将显示在文档大纲的第 1 级； 2 表示 2 级，依此类推。

## 例子

显示如何设置书签的大纲级别。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 插入一个书签，其中嵌套了另一个书签。
builder.StartBookmark("Bookmark 1");
builder.Writeln("Text inside Bookmark 1.");

builder.StartBookmark("Bookmark 2");
builder.Writeln("Text inside Bookmark 1 and 2.");
builder.EndBookmark("Bookmark 2");

builder.Writeln("Text inside Bookmark 1.");
builder.EndBookmark("Bookmark 1");

// 插入另一个书签。
builder.StartBookmark("Bookmark 3");
builder.Writeln("Text inside Bookmark 3.");
builder.EndBookmark("Bookmark 3");

// 当保存为 .pdf 时，书签可以通过下拉菜单访问，并被大多数读者用作锚点。
// 书签也可以有大纲级别的数值，
// 启用较低级别的大纲条目以在阅读器中折叠时隐藏较高级别的子条目。
PdfSaveOptions pdfSaveOptions = new PdfSaveOptions();
BookmarksOutlineLevelCollection outlineLevels = pdfSaveOptions.OutlineOptions.BookmarksOutlineLevels;

outlineLevels.Add("Bookmark 1", 1);
outlineLevels.Add("Bookmark 2", 2);
outlineLevels.Add("Bookmark 3", 3);

Assert.AreEqual(3, outlineLevels.Count);
Assert.True(outlineLevels.Contains("Bookmark 1"));
Assert.AreEqual(1, outlineLevels[0]);
Assert.AreEqual(2, outlineLevels["Bookmark 2"]);
Assert.AreEqual(2, outlineLevels.IndexOfKey("Bookmark 3"));

// 我们可以删除两个元素，以便只留下“书签 1”的大纲级别指定。
outlineLevels.RemoveAt(2);
outlineLevels.Remove("Bookmark 2");

// 有九个大纲级别。它们的编号将在保存操作期间进行优化。
// 在这种情况下，“5”和“9”级将变为“2”和“3”。
outlineLevels.Add("Bookmark 2", 5);
outlineLevels.Add("Bookmark 3", 9);

doc.Save(ArtifactsDir + "BookmarksOutlineLevelCollection.BookmarkLevels.pdf", pdfSaveOptions);

// 清空此集合将保留书签并将它们全部放在同一大纲级别。
outlineLevels.Clear();
```

### 也可以看看

* 命名空间 [Aspose.Words.Saving](../../aspose.words.saving/)
* 部件 [Aspose.Words](../../)
