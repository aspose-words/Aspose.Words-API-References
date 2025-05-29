---
title: DocumentBuilder.MoveToBookmark
linktitle: MoveToBookmark
articleTitle: MoveToBookmark
second_title: Aspose.Words for .NET
description: 使用 DocumentBuilder MoveToBookmark 方法轻松浏览您的文档，立即将光标定位在任何书签上以增强编辑。
type: docs
weight: 530
url: /zh/net/aspose.words/documentbuilder/movetobookmark/
---
## MoveToBookmark(*string*) {#movetobookmark}

将光标移动到书签。

```csharp
public bool MoveToBookmark(string bookmarkName)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| bookmarkName | String | 光标移动到的书签的名称。 |

### 返回值

`真的`如果找到书签；`错误的`否则。

## 评论

将光标移动到具有 the 指定名称的书签开头之后的位置。

比较不区分大小写。如果未找到书签，`错误的` is 返回并且光标没有移动。

插入新文本不会替换书签的现有文本。

请注意，文档中的某些书签已分配给表单字段。移动到此类书签并插入文本会将文本插入到 表单字段代码中。虽然这不会使表单字段失效，但插入的 文本将不可见，因为它已成为字段代码的一部分。

## 例子

展示如何将文档构建器的光标移动到文档中的不同节点。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 创建一个有效的书签，即由书签起始节点包围的节点组成的实体，
 // 以及书签结束节点。
builder.StartBookmark("MyBookmark");
builder.Write("Bookmark contents.");
builder.EndBookmark("MyBookmark");

NodeCollection firstParagraphNodes = doc.FirstSection.Body.FirstParagraph.GetChildNodes(NodeType.Any, false);

Assert.AreEqual(NodeType.BookmarkStart, firstParagraphNodes[0].NodeType);
Assert.AreEqual(NodeType.Run, firstParagraphNodes[1].NodeType);
Assert.AreEqual("Bookmark contents.", firstParagraphNodes[1].GetText().Trim());
Assert.AreEqual(NodeType.BookmarkEnd, firstParagraphNodes[2].NodeType);

// 文档构建器的光标始终位于我们最后添加的节点的前面。
// 如果构建器的光标位于文档的末尾，则其当前节点将为空。
// 前一个节点是我们最后添加的书签结束节点。
// 使用构建器添加新节点将把它们附加到最后一个节点。
Assert.Null(builder.CurrentNode);

// 如果我们希望使用构建器编辑文档的不同部分，
// 我们需要将光标移到我们想要编辑的节点上。
builder.MoveToBookmark("MyBookmark");

// 将其移动到书签将把它移动到书签开始和结束节点内的第一个节点，即封闭的运行。
Assert.AreEqual(firstParagraphNodes[1], builder.CurrentNode);

// 我们也可以像这样将光标移动到单个节点。
builder.MoveTo(doc.FirstSection.Body.FirstParagraph.GetChildNodes(NodeType.Any, false)[0]);

Assert.AreEqual(NodeType.BookmarkStart, builder.CurrentNode.NodeType);
Assert.AreEqual(doc.FirstSection.Body.FirstParagraph, builder.CurrentParagraph);
Assert.IsTrue(builder.IsAtStartOfParagraph);

// 我们可以使用特定的方法移动到文档的开始/结束。
builder.MoveToDocumentEnd();

Assert.IsTrue(builder.IsAtEndOfParagraph);

builder.MoveToDocumentStart();

Assert.IsTrue(builder.IsAtStartOfParagraph);
```

### 也可以看看

* class [DocumentBuilder](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)

---

## MoveToBookmark(*string, bool, bool*) {#movetobookmark_1}

将光标更精确地移动到书签。

```csharp
public bool MoveToBookmark(string bookmarkName, bool isStart, bool isAfter)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| bookmarkName | String | 光标移动到的书签的名称。 |
| isStart | Boolean | 什么时候`真的` ，将光标移动到书签的开头。 当`错误的`，将光标移动到书签的末尾。 |
| isAfter | Boolean | 什么时候`真的` ，将光标移动到 bookmark 的开始或结束位置之后。当`错误的`，将光标移动到 bookmark 开始或结束位置之前。 |

### 返回值

`真的`如果找到书签；`错误的`否则。

## 评论

将光标移动到书签开始或结束之前或之后的位置。

如果所需位置不在内联级别，则移动到下一段。

比较不区分大小写。如果未找到书签，`错误的` is 返回并且光标没有移动。

## 例子

展示如何将文档构建器的节点插入点光标移动到书签。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 一个有效的书签由一个 BookmarkStart 节点、一个 BookmarkEnd 节点和一个
// 随后在某处匹配书签名称，以及这些节点所包含的内容。
builder.StartBookmark("MyBookmark");
builder.Write("Hello world! ");
builder.EndBookmark("MyBookmark");

// 有 4 种方法可以将文档构建器的光标移动到书签。
// 如果我们位于 BookmarkStart 和 BookmarkEnd 节点之间，则光标将位于书签内。
// 这意味着构建器添加的任何文本都将成为书签的一部分。
// 1 - 在书签之外，在 BookmarkStart 节点前面：
Assert.True(builder.MoveToBookmark("MyBookmark", true, false));
builder.Write("1. ");

Assert.AreEqual("Hello world! ", doc.Range.Bookmarks["MyBookmark"].Text);
Assert.AreEqual("1. Hello world!", doc.GetText().Trim());

// 2 - 在书签内，紧接着 BookmarkStart 节点：
Assert.True(builder.MoveToBookmark("MyBookmark", true, true));
builder.Write("2. ");

Assert.AreEqual("2. Hello world! ", doc.Range.Bookmarks["MyBookmark"].Text);
Assert.AreEqual("1. 2. Hello world!", doc.GetText().Trim());

// 2 - 在书签内，就在 BookmarkEnd 节点前面：
Assert.True(builder.MoveToBookmark("MyBookmark", false, false));
builder.Write("3. ");

Assert.AreEqual("2. Hello world! 3. ", doc.Range.Bookmarks["MyBookmark"].Text);
Assert.AreEqual("1. 2. Hello world! 3.", doc.GetText().Trim());

// 4 - 在书签之外，在 BookmarkEnd 节点之后：
Assert.True(builder.MoveToBookmark("MyBookmark", false, true));
builder.Write("4.");

Assert.AreEqual("2. Hello world! 3. ", doc.Range.Bookmarks["MyBookmark"].Text);
Assert.AreEqual("1. 2. Hello world! 3. 4.", doc.GetText().Trim());
```

### 也可以看看

* class [DocumentBuilder](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
