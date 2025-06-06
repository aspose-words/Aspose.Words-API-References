---
title: BookmarksOutlineLevelCollection.Add
linktitle: Add
articleTitle: Add
second_title: Aspose.Words for .NET
description: 了解如何使用 BookmarksOutlineLevelCollection Add 方法增强您的项目，轻松地将书签添加到您的收藏夹中以便更好地组织。
type: docs
weight: 40
url: /zh/net/aspose.words.saving/bookmarksoutlinelevelcollection/add/
---
## BookmarksOutlineLevelCollection.Add method

将书签添加到收藏夹。

```csharp
public void Add(string name, int outlineLevel)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| name | String | 要添加的书签的名称（不区分大小写）。 |
| outlineLevel | Int32 | 书签的大纲级别。有效范围为 0 到 9。 |

## 例子

展示如何设置书签的大纲级别。

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

// 保存为 .pdf 时，大多数读者可以通过下拉菜单访问书签并将其用作锚点。
// 书签也可以有大纲级别的数值，
// 使较低级别的大纲条目在阅读器中折叠时隐藏较高级别的子条目。
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

// 大纲级别共有九个。保存操作期间，它们的编号将会进行优化。
// 在这种情况下，级别“5”和“9”将变为“2”和“3”。
outlineLevels.Add("Bookmark 2", 5);
outlineLevels.Add("Bookmark 3", 9);

doc.Save(ArtifactsDir + "BookmarksOutlineLevelCollection.BookmarkLevels.pdf", pdfSaveOptions);

// 清空此集合将保留书签并将它们全部放在同一大纲级别。
outlineLevels.Clear();
```

### 也可以看看

* class [BookmarksOutlineLevelCollection](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
