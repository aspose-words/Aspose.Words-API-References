---
title: DocumentBuilder.MoveTo
linktitle: MoveTo
articleTitle: MoveTo
second_title: Aspose.Words for .NET
description: 探索 DocumentBuilder MoveTo 方法，轻松导航内联节点并有效地将光标定位在段落末尾，以实现无缝文档编辑。
type: docs
weight: 520
url: /zh/net/aspose.words/documentbuilder/moveto/
---
## DocumentBuilder.MoveTo method

将光标移动到内联节点或段落末尾。

```csharp
public void MoveTo(Node node)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| node | Node | 该节点必须是段落或段落的直接子节点。 |

## 评论

什么时候节点是内联级节点，光标将移动到此节点 ，并且更多内容将插入该节点之前。

什么时候节点是一个[`Paragraph`](../../paragraph/)，光标将移动到段落末尾 ，并且后续内容将在段落分隔符之前插入。

什么时候节点是块级节点，但不是[`Paragraph`](../../paragraph/)，光标将移动到第一个段落的末尾，进入块级 node ，并且后续内容将在段落分隔符之前插入。

## 例子

展示如何将 DocumentBuilder 的光标位置移动到指定节点。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Run 1. ");

// 文档构建器有一个游标，它充当文档的一部分
// 当我们使用其文档构造方法时，构建器会附加新节点。
// 此光标的功能与 Microsoft Word 的闪烁光标相同，
// 并且它也总是在构建器刚刚插入的任何节点之后立即结束。
// 要将内容附加到文档的不同部分，
// 我们可以使用“MoveTo”方法将光标移动到不同的节点。
builder.MoveTo(doc.FirstSection.Body.FirstParagraph.Runs[0]);
// 光标现在位于我们将其移动到的节点前面。
// 添加第二个运行将会把它插入到第一个运行的前面。
builder.Writeln("Run 2. ");

Assert.AreEqual("Run 2. \rRun 1.", doc.GetText().Trim());

// 将光标移动到文档末尾，像之前一样继续将文本附加到末尾。
builder.MoveTo(doc.LastSection.Body.LastParagraph);
builder.Writeln("Run 3. ");

Assert.AreEqual("Run 2. \rRun 1. \rRun 3.", doc.GetText().Trim());
```

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

* class [Node](../../node/)
* class [DocumentBuilder](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
