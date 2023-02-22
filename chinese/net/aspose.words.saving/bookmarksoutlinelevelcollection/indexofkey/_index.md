---
title: BookmarksOutlineLevelCollection.IndexOfKey
second_title: Aspose.Words for .NET API 参考
description: BookmarksOutlineLevelCollection 方法. 返回集合中指定书签的从零开始的索引
type: docs
weight: 80
url: /zh/net/aspose.words.saving/bookmarksoutlinelevelcollection/indexofkey/
---
## BookmarksOutlineLevelCollection.IndexOfKey method

返回集合中指定书签的从零开始的索引。

```csharp
public int IndexOfKey(string name)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| name | String | 书签的不区分大小写的名称。 |

### 返回值

从零开始的索引。如果未找到，则为负值。

### 例子

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

* class [BookmarksOutlineLevelCollection](../)
* 命名空间 [Aspose.Words.Saving](../../bookmarksoutlinelevelcollection/)
* 部件 [Aspose.Words](../../../)


