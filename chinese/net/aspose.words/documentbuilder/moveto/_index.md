---
title: DocumentBuilder.MoveTo
second_title: Aspose.Words for .NET API 参考
description: DocumentBuilder 方法. 将光标移动到内联节点或段落末尾
type: docs
weight: 460
url: /zh/net/aspose.words/documentbuilder/moveto/
---
## DocumentBuilder.MoveTo method

将光标移动到内联节点或段落末尾。

```csharp
public void MoveTo(Node node)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| node | Node | 节点必须是段落或段落的直接子级。 |

### 评论

什么时候节点是一个内联级节点，光标移动到这个 node 并且将在该节点之前插入更多内容。

什么时候节点是一个 **段落**光标移动到段落 的末尾，并且将在段落分隔符之前插入更多内容。

什么时候节点是块级节点但不是段落，光标移动到第一段的末尾进入块级节点 ，并且将在段落中断之前插入更多内容。

### 例子

显示如何将 DocumentBuilder 的光标位置移动到指定节点。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Run 1. ");

// 文档构建器有一个游标，它充当文档的一部分
// 当我们使用它的文档构造方法时，构建器会在其中追加新节点。
// 此光标的功能与 Microsoft Word 的闪烁光标相同，
// 它也总是在构建器刚刚插入的任何节点之后立即结束。
// 将内容附加到文档的不同部分，
// 我们可以使用“MoveTo”方法将光标移动到不同的节点。
// 光标现在位于我们移动到的节点的前面。
// 添加第二次运行会将其插入到第一次运行的前面。
builder.Writeln("Run 2. ");

Assert.AreEqual("Run 2. \rRun 1.", doc.GetText().Trim());

// 将光标移动到文档的末尾以继续像以前一样将文本附加到末尾。
builder.MoveTo(doc.LastSection.Body.LastParagraph);
builder.Writeln("Run 3. ");

Assert.AreEqual("Run 2. \rRun 1. \rRun 3.", doc.GetText().Trim());
```

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

* class [Node](../../node/)
* class [DocumentBuilder](../)
* 命名空间 [Aspose.Words](../../documentbuilder/)
* 部件 [Aspose.Words](../../../)


