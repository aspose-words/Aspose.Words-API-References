---
title: Section.EnsureMinimum
linktitle: EnsureMinimum
articleTitle: EnsureMinimum
second_title: Aspose.Words for .NET
description: 使用 EnsureMinimum 方法优化您的内容，确保每个部分都包含一个带有段落的正文，以增强清晰度和结构。
type: docs
weight: 150
url: /zh/net/aspose.words/section/ensureminimum/
---
## Section.EnsureMinimum method

确保该部分具有[`Body`](../body/)有一个[`Paragraph`](../../paragraph/).

```csharp
public void EnsureMinimum()
```

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

* class [Section](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
