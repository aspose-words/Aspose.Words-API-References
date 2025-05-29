---
title: Document.EnsureMinimum
linktitle: EnsureMinimum
articleTitle: EnsureMinimum
second_title: Aspose.Words for .NET
description: 了解如何使用 EnsureMinimum 方法自动在文档中创建章节和段落，确保内容完整且有序。
type: docs
weight: 620
url: /zh/net/aspose.words/document/ensureminimum/
---
## Document.EnsureMinimum method

如果文档不包含任何章节，则创建一个包含一个段落的章节。

```csharp
public void EnsureMinimum()
```

## 例子

展示如何确保文档包含编辑其内容所需的最小节点集。

```csharp
// 新建一个文档，其中包含一个子Section，该Section又包含一个子Body和一个子Paragraph。
// 我们可以通过向该段落添加诸如 Runs 或内联形状之类的节点来编辑文档主体的内容。
Document doc = new Document();
NodeCollection nodes = doc.GetChildNodes(NodeType.Any, true);

Assert.AreEqual(NodeType.Section, nodes[0].NodeType);
Assert.AreEqual(doc, nodes[0].ParentNode);

Assert.AreEqual(NodeType.Body, nodes[1].NodeType);
Assert.AreEqual(nodes[0], nodes[1].ParentNode);

Assert.AreEqual(NodeType.Paragraph, nodes[2].NodeType);
Assert.AreEqual(nodes[1], nodes[2].ParentNode);

// 这是我们编辑文档所需的最小节点集。
// 如果我们删除其中任何一个，我们将无法再编辑该文档。
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
