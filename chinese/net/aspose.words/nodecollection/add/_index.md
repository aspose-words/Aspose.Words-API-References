---
title: NodeCollection.Add
linktitle: Add
articleTitle: Add
second_title: Aspose.Words for .NET
description: 探索 NodeCollection Add 方法，轻松地将节点附加到您的集合中，轻松高效地增强您的数据管理。
type: docs
weight: 30
url: /zh/net/aspose.words/nodecollection/add/
---
## NodeCollection.Add method

在集合末尾添加一个节点。

```csharp
public void Add(Node node)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| node | Node | 要添加到集合末尾的节点。 |

### 例外

| 例外 | （健康）状况 |
| --- | --- |
| NotSupportedException | 这[`NodeCollection`](../)是一个“深度”收藏。 |

## 评论

该节点作为子节点插入到创建集合的节点对象中。

如果插入的节点是从另一个文档创建的，则应使用 [`ImportNode`](../../documentbase/importnode/)将节点导入当前文档。 然后可以将导入的节点插入到当前文档中。

## 例子

展示如何准备新的部分节点以供编辑。

```csharp
Document doc = new Document();

// 空白文档带有一个部分，该部分有一个正文，该正文又有一个段落。
// 我们可以通过向该段落添加文本、形状或表格等元素来向该文档添加内容。
Assert.AreEqual(NodeType.Section, doc.GetChild(NodeType.Any, 0, true).NodeType);
Assert.AreEqual(NodeType.Body, doc.Sections[0].GetChild(NodeType.Any, 0, true).NodeType);
Assert.AreEqual(NodeType.Paragraph, doc.Sections[0].Body.GetChild(NodeType.Any, 0, true).NodeType);

// 如果我们添加这样的新部分，它将没有主体或任何其他子节点。
doc.Sections.Add(new Section(doc));

Assert.AreEqual(0, doc.Sections[1].GetChildNodes(NodeType.Any, true).Count);

// 运行“EnsureMinimum”方法向此部分添加正文和段落以开始编辑它。
doc.LastSection.EnsureMinimum();

Assert.AreEqual(NodeType.Body, doc.Sections[1].GetChild(NodeType.Any, 0, true).NodeType);
Assert.AreEqual(NodeType.Paragraph, doc.Sections[1].Body.GetChild(NodeType.Any, 0, true).NodeType);

doc.Sections[0].Body.FirstParagraph.AppendChild(new Run(doc, "Hello world!"));

Assert.AreEqual("Hello world!", doc.GetText().Trim());
```

### 也可以看看

* class [Node](../../node/)
* class [NodeCollection](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
