---
title: DocumentBuilder.MoveToBookmark
linktitle: MoveToBookmark
articleTitle: MoveToBookmark
second_title: 用于 .NET 的 Aspose.Words
description: DocumentBuilder MoveToBookmark 方法. 将光标移动到书签 在 C#.
type: docs
weight: 490
url: /zh/net/aspose.words/documentbuilder/movetobookmark/
---
## MoveToBookmark(*string*) {#movetobookmark}

将光标移动到书签。

```csharp
public bool MoveToBookmark(string bookmarkName)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| bookmarkName | String | 要将光标移动到的书签的名称。 |

### 返回值

如果找到书签，则为真；否则为假。

## 评论

将光标移动到带有指定名称的 书签开始之后的位置。

比较不区分大小写。如果未找到书签，则返回 false is 并且不移动光标。

插入新文本不会替换书签的现有文本。

请注意，文档中的某些书签已分配给表单域。 移动到此类书签并在其中插入文本会将文本插入到 表单域代码中。尽管这不会使表单域无效，但inserted 文本将不可见，因为它成为域代码的一部分。

## 例子

显示如何将文档构建器的光标移动到文档中的不同节点。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 创建一个有效的书签，一个由书签开始节点包围的节点组成的实体，
 // 和一个书签结束节点。
builder.StartBookmark("MyBookmark");
builder.Write("Bookmark contents.");
builder.EndBookmark("MyBookmark");

NodeCollection firstParagraphNodes = doc.FirstSection.Body.FirstParagraph.ChildNodes;

Assert.AreEqual(NodeType.BookmarkStart, firstParagraphNodes[0].NodeType);
Assert.AreEqual(NodeType.Run, firstParagraphNodes[1].NodeType);
Assert.AreEqual("Bookmark contents.", firstParagraphNodes[1].GetText().Trim());
Assert.AreEqual(NodeType.BookmarkEnd, firstParagraphNodes[2].NodeType);

// 文档构建器的光标始终位于我们最后添加的节点之前。
// 如果构建器的光标位于文档的末尾，则其当前节点将为空。
// 上一个节点是我们最后添加的书签结束节点。
// 使用构建器添加新节点会将它们附加到最后一个节点。
Assert.Null(builder.CurrentNode);

// 如果我们希望使用构建器编辑文档的不同部分，
// 我们需要把它的光标带到我们想要编辑的节点上。
builder.MoveToBookmark("MyBookmark");

// 将其移动到书签会将其移动到书签开始和结束节点中的第一个节点，即封闭的运行。
Assert.AreEqual(firstParagraphNodes[1], builder.CurrentNode);

// 我们也可以像这样将光标移动到单个节点上。
builder.MoveTo(doc.FirstSection.Body.FirstParagraph.GetChildNodes(NodeType.Any, false)[0]);

Assert.AreEqual(NodeType.BookmarkStart, builder.CurrentNode.NodeType);
Assert.AreEqual(doc.FirstSection.Body.FirstParagraph, builder.CurrentParagraph);
Assert.IsTrue(builder.IsAtStartOfParagraph);

// 我们可以使用特定的方法移动到文档的开头/结尾。
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

将光标移动到更精确的书签。

```csharp
public bool MoveToBookmark(string bookmarkName, bool isStart, bool isAfter)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| bookmarkName | String | 要将光标移动到的书签的名称。 |
| isStart | Boolean | 如果为 true，则将光标移动到书签的开头。 如果为 false，则将光标移动到书签的末尾。 |
| isAfter | Boolean | 如果为 true，则将光标移动到 bookmark 开始或结束位置之后。如果为 false，则将光标移动到 bookmark 开始或结束位置之前。 |

### 返回值

如果找到书签，则为真；否则为假。

## 评论

将光标移动到书签开始或结束之前或之后的位置。

如果所需位置不在行内级别，则移至下一段。

比较不区分大小写。如果未找到书签，则返回 false is 并且不移动光标。

## 例子

显示如何将文档构建器的节点插入点光标移动到书签。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 一个有效的书签由一个 BookmarkStart 节点、一个 BookmarkEnd 节点和一个
// 之后某处匹配书签名称，以及这些节点所包含的内容。
builder.StartBookmark("MyBookmark");
builder.Write("Hello world! ");
builder.EndBookmark("MyBookmark");

// 将文档构建器的光标移动到书签有 4 种方法。
// 如果我们在 BookmarkStart 和 BookmarkEnd 节点之间，光标将在书签内。
// 这意味着构建器添加的任何文本都将成为书签的一部分。
// 1 - 在书签之外，在 BookmarkStart 节点之前：
Assert.True(builder.MoveToBookmark("MyBookmark", true, false));
builder.Write("1. ");

Assert.AreEqual("Hello world! ", doc.Range.Bookmarks["MyBookmark"].Text);
Assert.AreEqual("1. Hello world!", doc.GetText().Trim());

// 2 - 在书签内，就在 BookmarkStart 节点之后：
Assert.True(builder.MoveToBookmark("MyBookmark", true, true));
builder.Write("2. ");

Assert.AreEqual("2. Hello world! ", doc.Range.Bookmarks["MyBookmark"].Text);
Assert.AreEqual("1. 2. Hello world!", doc.GetText().Trim());

// 2 - 在书签内，BookmarkEnd 节点的正前方：
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
