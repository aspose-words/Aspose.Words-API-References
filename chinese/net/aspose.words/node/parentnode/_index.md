---
title: Node.ParentNode
linktitle: ParentNode
articleTitle: ParentNode
second_title: Aspose.Words for .NET
description: 发现 Node ParentNode 属性可以轻松访问任何节点的直接父节点，从而提高您的 Web 开发效率和代码清晰度。
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

如果一个节点刚刚被创建但尚未添加到树中， 或者它已经从树中删除，则父节点是`无效的`。

## 例子

显示如何访问节点的父节点。

```csharp
Document doc = new Document();
Paragraph para = doc.FirstSection.Body.FirstParagraph;

// 将子 Run 节点附加到文档的第一段。
Run run = new Run(doc, "Hello world!");
para.AppendChild(run);

// 段落是运行节点的父节点。我们可以追溯这个血统
// 一直到文档节点，它是文档节点树的根。
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

* class [CompositeNode](../../compositenode/)
* class [Node](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
