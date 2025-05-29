---
title: DocumentBuilder.EndBookmark
linktitle: EndBookmark
articleTitle: EndBookmark
second_title: Aspose.Words for .NET
description: 使用 DocumentBuilder 的 EndBookmark 方法轻松标记文档中书签的结尾，增强文档的组织和导航。
type: docs
weight: 210
url: /zh/net/aspose.words/documentbuilder/endbookmark/
---
## DocumentBuilder.EndBookmark method

将文档中的当前位置标记为书签结束。

```csharp
public BookmarkEnd EndBookmark(string bookmarkName)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| bookmarkName | String | 书签的名称。 |

### 返回值

刚刚创建的书签结束节点。

## 评论

文档中的书签可以重叠并跨越任意范围。要创建有效的书签，您需要同时调用[`StartBookmark`](../startbookmark/)和`EndBookmark`同样的*bookmarkName* 参数。

保存文档时，格式不正确的书签或名称重复的书签将被忽略。

## 例子

显示如何创建书签。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 有效的书签需要包含文档正文
// 使用匹配的书签名称创建的 BookmarkStart 和 BookmarkEnd 节点。
builder.StartBookmark("MyBookmark");
builder.Writeln("Hello world!");
builder.EndBookmark("MyBookmark");

Assert.AreEqual(1, doc.Range.Bookmarks.Count);
Assert.AreEqual("MyBookmark", doc.Range.Bookmarks[0].Name);
Assert.AreEqual("Hello world!", doc.Range.Bookmarks[0].Text.Trim());
```

展示如何插入引用本地书签的超链接。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.StartBookmark("Bookmark1");
builder.Write("Bookmarked text. ");
builder.EndBookmark("Bookmark1");
builder.Writeln("Text outside of the bookmark.");

// 插入一个超链接字段，链接到书签。我们可以传递字段开关
// 作为包含所引用书签名称的参数的一部分传递给“InsertHyperlink”方法。
builder.Font.Color = Color.Blue;
builder.Font.Underline = Underline.Single;
FieldHyperlink hyperlink = (FieldHyperlink)builder.InsertHyperlink("Link to Bookmark1", "Bookmark1", true);
hyperlink.ScreenTip = "Hyperlink Tip";

doc.Save(ArtifactsDir + "DocumentBuilder.InsertHyperlinkToLocalBookmark.docx");
```

### 也可以看看

* class [BookmarkEnd](../../bookmarkend/)
* class [DocumentBuilder](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
