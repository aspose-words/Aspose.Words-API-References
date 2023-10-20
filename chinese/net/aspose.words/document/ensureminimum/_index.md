---
title: Document.EnsureMinimum
linktitle: EnsureMinimum
articleTitle: EnsureMinimum
second_title: 用于 .NET 的 Aspose.Words
description: Document EnsureMinimum 方法. 如果文档不包含任何节则创建一个包含一个段落的节 在 C#.
type: docs
weight: 580
url: /zh/net/aspose.words/document/ensureminimum/
---
## Document.EnsureMinimum method

如果文档不包含任何节，则创建一个包含一个段落的节。

```csharp
public void EnsureMinimum()
```

## 例子

演示如何确保文档包含编辑其内容所需的最小节点集。

```csharp
// 新创建的文档包含一个子Section，其中包含一个子Body 和一个子Paragraph。
// 我们可以通过向该段落添加节点（例如 Runs 或内联 Shapes）来编辑文档正文的内容。
Document doc = new Document();
NodeCollection nodes = doc.GetChildNodes(NodeType.Any, true);

Assert.AreEqual(NodeType.Section, nodes[0].NodeType);
Assert.AreEqual(doc, nodes[0].ParentNode);

Assert.AreEqual(NodeType.Body, nodes[1].NodeType);
Assert.AreEqual(nodes[0], nodes[1].ParentNode);

Assert.AreEqual(NodeType.Paragraph, nodes[2].NodeType);
Assert.AreEqual(nodes[1], nodes[2].ParentNode);

// 这是我们编辑文档所需的最小节点集。
// 如果删除其中任何一个，我们将无法再编辑文档。
doc.RemoveAllChildren();

Assert.AreEqual(0, doc.GetChildNodes(NodeType.Any, true).Count);

// 调用此方法以确保文档至少具有这三个节点，以便我们可以再次编辑它。
doc.EnsureMinimum();

Assert.AreEqual(NodeType.Section, nodes[0].NodeType);
Assert.AreEqual(NodeType.Body, nodes[1].NodeType);
Assert.AreEqual(NodeType.Paragraph, nodes[2].NodeType);

((Paragraph)nodes[2]).Runs.Add(new Run(doc, "Hello world!"));
```

### 也可以看看

* class [Document](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
