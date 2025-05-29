---
title: Node.Document
linktitle: Document
articleTitle: Document
second_title: Aspose.Words for .NET
description: 发现节点文档属性，轻松访问链接到节点的文档，实现无缝数据管理并提高生产力。
type: docs
weight: 20
url: /zh/net/aspose.words/node/document/
---
## Node.Document property

获取此节点所属的文档。

```csharp
public virtual DocumentBase Document { get; }
```

## 评论

即使节点刚刚被创建 并且尚未添加到树中，或者已经从树中删除，它也始终属于一个文档。

## 例子

展示如何创建节点并设置其所属文档。

```csharp
Document doc = new Document();
Paragraph para = new Paragraph(doc);
para.AppendChild(new Run(doc, "Hello world!"));

// 我们尚未将此段落作为子节点附加到任何复合节点。
Assert.IsNull(para.ParentNode);

// 如果一个节点是另一个复合节点的适当子节点类型，
// 只有当两个节点具有相同的所有者文档时，我们才能将其作为子节点附加。
// 所有者文档是我们传递给节点构造函数的文档。
// 我们没有将此段落附加到文档，因此文档不包含其文本。
Assert.AreEqual(para.Document, doc);
Assert.AreEqual(string.Empty, doc.GetText().Trim());

// 由于该文档拥有此段落，我们可以将其一种样式应用于该段落的内容。
para.ParagraphFormat.Style = doc.Styles["Heading 1"];

// 将此节点添加到文档，然后验证其内容。
doc.FirstSection.Body.AppendChild(para);

Assert.AreEqual(doc.FirstSection.Body, para.ParentNode);
Assert.AreEqual("Hello world!", doc.GetText().Trim());
```

### 也可以看看

* class [DocumentBase](../../documentbase/)
* class [Node](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
