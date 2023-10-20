---
title: BookmarksOutlineLevelCollection.Contains
linktitle: Contains
articleTitle: Contains
second_title: 用于 .NET 的 Aspose.Words
description: BookmarksOutlineLevelCollection Contains 方法. 确定集合中是否包含具有给定名称的书签 在 C#.
type: docs
weight: 60
url: /zh/net/aspose.words.saving/bookmarksoutlinelevelcollection/contains/
---
## BookmarksOutlineLevelCollection.Contains method

确定集合中是否包含具有给定名称的书签。

```csharp
public bool Contains(string name)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| name | String | 要查找的书签名称，不区分大小写。 |

### 返回值

`真的`如果在集合中找到项目；否则，`错误的`。

## 例子

演示如何设置书签的大纲级别。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 插入一个书签，其中嵌套另一个书签。
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

// 保存为 .pdf 时，可以通过下拉菜单访问书签，并被大多数读者用作锚点。
// 书签也可以有大纲级别的数值，
// 启用较低级别的大纲条目，以便在阅读器中折叠时隐藏较高级别的子条目。
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

// 我们可以删除两个元素，以便仅留下“书签 1”的大纲级别指定。
outlineLevels.RemoveAt(2);
outlineLevels.Remove("Bookmark 2");

// 有九个大纲级别。它们的编号将在保存操作期间进行优化。
// 在这种情况下，级别“5”和“9”将变为“2”和“3”。
outlineLevels.Add("Bookmark 2", 5);
outlineLevels.Add("Bookmark 3", 9);

doc.Save(ArtifactsDir + "BookmarksOutlineLevelCollection.BookmarkLevels.pdf", pdfSaveOptions);

// 清空此集合将保留书签并将它们全部放在同一大纲级别上。
outlineLevels.Clear();
```

### 也可以看看

* class [BookmarksOutlineLevelCollection](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
