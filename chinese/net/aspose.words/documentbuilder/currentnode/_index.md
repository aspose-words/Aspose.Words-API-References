---
title: DocumentBuilder.CurrentNode
linktitle: CurrentNode
articleTitle: CurrentNode
second_title: 用于 .NET 的 Aspose.Words
description: DocumentBuilder CurrentNode 财产. 获取当前在此 DocumentBuilder 中选择的节点 在 C#.
type: docs
weight: 40
url: /zh/net/aspose.words/documentbuilder/currentnode/
---
## DocumentBuilder.CurrentNode property

获取当前在此 DocumentBuilder 中选择的节点。

```csharp
public Node CurrentNode { get; }
```

## 评论

`CurrentNode`是一个游标[`DocumentBuilder`](../)并指向一个[`Node`](../../node/) 是 a 的直接子代[`Paragraph`](../../paragraph/)。您使用 执行的任何插入操作[`DocumentBuilder`](../)将在之前插入`CurrentNode`。

当当前段落为空或光标位于段落或结构化文档标记末尾之前 时，`CurrentNode`回报`无效的`。

## 例子

演示如何将文档生成器的光标移动到文档中的不同节点。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 创建一个有效的书签，一个由书签起始节点包围的节点组成的实体，
 // 和一个书签结束节点。
builder.StartBookmark("MyBookmark");
builder.Write("Bookmark contents.");
builder.EndBookmark("MyBookmark");

NodeCollection firstParagraphNodes = doc.FirstSection.Body.FirstParagraph.GetChildNodes(NodeType.Any, false);

Assert.AreEqual(NodeType.BookmarkStart, firstParagraphNodes[0].NodeType);
Assert.AreEqual(NodeType.Run, firstParagraphNodes[1].NodeType);
Assert.AreEqual("Bookmark contents.", firstParagraphNodes[1].GetText().Trim());
Assert.AreEqual(NodeType.BookmarkEnd, firstParagraphNodes[2].NodeType);

// 文档构建器的光标始终位于我们最后添加的节点之前。
// 如果构建器的光标位于文档末尾，则其当前节点将为空。
// 前一个节点是我们最后添加的书签结束节点。
// 使用构建器添加新节点会将它们附加到最后一个节点。
Assert.Null(builder.CurrentNode);

// 如果我们希望使用构建器编辑文档的不同部分，
// 我们需要将光标移至我们想要编辑的节点。
builder.MoveToBookmark("MyBookmark");

// 将其移动到书签会将其移动到书签开始和结束节点中的第一个节点，即封闭的运行。
Assert.AreEqual(firstParagraphNodes[1], builder.CurrentNode);

// 我们也可以像这样将光标移动到单个节点。
builder.MoveTo(doc.FirstSection.Body.FirstParagraph.GetChildNodes(NodeType.Any, false)[0]);

Assert.AreEqual(NodeType.BookmarkStart, builder.CurrentNode.NodeType);
Assert.AreEqual(doc.FirstSection.Body.FirstParagraph, builder.CurrentParagraph);
Assert.IsTrue(builder.IsAtStartOfParagraph);

// 我们可以使用特定的方法来移动到文档的开头/结尾。
builder.MoveToDocumentEnd();

Assert.IsTrue(builder.IsAtEndOfParagraph);

builder.MoveToDocumentStart();

Assert.IsTrue(builder.IsAtStartOfParagraph);
```

### 也可以看看

* class [Node](../../node/)
* class [DocumentBuilder](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
