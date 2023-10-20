---
title: Node.ParentNode
linktitle: ParentNode
articleTitle: ParentNode
second_title: 用于 .NET 的 Aspose.Words
description: Node ParentNode 财产. 获取此节点的直接父节点 在 C#.
type: docs
weight: 60
url: /zh/net/aspose.words/node/parentnode/
---
## Node.ParentNode property

获取此节点的直接父节点。

```csharp
public CompositeNode ParentNode { get; }
```

## 评论

如果一个节点刚刚创建并且尚未添加到树中， 或者如果它已从树中删除，则父节点为空。

## 例子

显示如何访问节点的父节点。

```csharp
Document doc = new Document();
Paragraph para = doc.FirstSection.Body.FirstParagraph;

// 将一个子 Run 节点附加到文档的第一段。
Run run = new Run(doc, "Hello world!");
para.AppendChild(run);

// 段落是运行节点的父节点。我们可以追溯这个血统
// 一直到文档节点，它是文档的节点树的根。
Assert.AreEqual(para, run.ParentNode);
Assert.AreEqual(doc.FirstSection.Body, para.ParentNode);
Assert.AreEqual(doc.FirstSection, doc.FirstSection.Body.ParentNode);
Assert.AreEqual(doc, doc.FirstSection.ParentNode);
```

展示如何创建节点并设置其所属文档。

```csharp
Document doc = new Document();
Paragraph para = new Paragraph(doc);
para.AppendChild(new Run(doc, "Hello world!"));

// 我们还没有将此段落作为子节点附加到任何复合节点。
Assert.IsNull(para.ParentNode);

// 如果一个节点是另一个复合节点的合适的子节点类型，
// 只有当两个节点具有相同的所有者文档时，我们才能将其作为子节点附加。
// 所有者文档是我们传递给节点构造函数的文档。
// 我们没有将此段落附加到文档中，因此文档不包含其文本。
Assert.AreEqual(para.Document, doc);
Assert.AreEqual(string.Empty, doc.GetText().Trim());

// 由于文档拥有这个段落，我们可以将它的一种样式应用于段落的内容。
para.ParagraphFormat.Style = doc.Styles["Heading 1"];

// 将此节点添加到文档中，然后验证其内容。
doc.FirstSection.Body.AppendChild(para);

Assert.AreEqual(doc.FirstSection.Body, para.ParentNode);
Assert.AreEqual("Hello world!", doc.GetText().Trim());
```

### 也可以看看

* class [CompositeNode](../../compositenode/)
* class [Node](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
