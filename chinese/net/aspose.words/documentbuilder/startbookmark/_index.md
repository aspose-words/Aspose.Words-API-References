---
title: DocumentBuilder.StartBookmark
second_title: Aspose.Words for .NET API 参考
description: DocumentBuilder 方法. 将文档中的当前位置标记为书签开始
type: docs
weight: 580
url: /zh/net/aspose.words/documentbuilder/startbookmark/
---
## DocumentBuilder.StartBookmark method

将文档中的当前位置标记为书签开始。

```csharp
public BookmarkStart StartBookmark(string bookmarkName)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| bookmarkName | String | 书签的名称。 |

### 返回值

刚刚创建的书签开始节点。

### 评论

文档中的书签可以重叠并跨越任何范围。要创建有效的书签，您需要 to 调用两者`StartBookmark`和[`EndBookmark`](../endbookmark/)同 **书签名称** 参数。

保存文档时将忽略格式错误的书签或具有重复名称的书签。

### 例子

显示如何创建书签。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 一个有效的书签需要有文档正文
// 使用匹配的书签名称创建的 BookmarkStart 和 BookmarkEnd 节点。
builder.StartBookmark("MyBookmark");
builder.Writeln("Hello world!");
builder.EndBookmark("MyBookmark");

Assert.AreEqual(1, doc.Range.Bookmarks.Count);
Assert.AreEqual("MyBookmark", doc.Range.Bookmarks[0].Name);
Assert.AreEqual("Hello world!", doc.Range.Bookmarks[0].Text.Trim());
```

演示如何插入引用本地书签的超链接。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.StartBookmark("Bookmark1");
builder.Write("Bookmarked text. ");
builder.EndBookmark("Bookmark1");
builder.Writeln("Text outside of the bookmark.");

// 插入一个链接到书签的 HYPERLINK 字段。我们可以通过字段开关
// 将“InsertHyperlink”方法作为包含引用书签名称的参数的一部分。
builder.Font.Color = Color.Blue;
builder.Font.Underline = Underline.Single;
builder.InsertHyperlink("Link to Bookmark1", @"Bookmark1"" \o ""Hyperlink Tip", true);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertHyperlinkToLocalBookmark.docx");
```

### 也可以看看

* class [BookmarkStart](../../bookmarkstart/)
* class [DocumentBuilder](../)
* 命名空间 [Aspose.Words](../../documentbuilder/)
* 部件 [Aspose.Words](../../../)


