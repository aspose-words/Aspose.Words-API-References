---
title: SectionCollection.Item
second_title: Aspose.Words for .NET API 参考
description: SectionCollection 财产. 检索给定索引处的节
type: docs
weight: 10
url: /zh/net/aspose.words/sectioncollection/item/
---
## SectionCollection indexer

检索给定索引处的节。

```csharp
public Section this[int index] { get; }
```

| 范围 | 描述 |
| --- | --- |
| index | 节列表的索引。 |

### 评论

该索引是从零开始的。

允许使用负索引，并指示从集合的后面进行访问。 例如 -1 表示最后一项，-2 表示最后一项，依此类推。

如果索引大于或等于列表中的项目数，则返回空引用。

如果索引为负并且其绝对值大于列表中的项目数，则返回空引用。

### 例子

显示何时重新计算文档的页面布局。

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// 第一次将文档保存为 PDF、图像或打印
// 在其页面中缓存文档的布局。
doc.Save(ArtifactsDir + "Document.UpdatePageLayout.1.pdf");

// 以某种方式修改文档。
doc.Styles["Normal"].Font.Size = 6;
doc.Sections[0].PageSetup.Orientation = Aspose.Words.Orientation.Landscape;
doc.Sections[0].PageSetup.Margins = Margins.Mirrored;

 // 在当前版本的Aspose.Words中，修改文档不会自动重建
// 缓存的页面布局。如果我们希望缓存布局
// 为了保持最新状态，我们需要手动更新它。
doc.UpdatePageLayout();

doc.Save(ArtifactsDir + "Document.UpdatePageLayout.2.pdf");
```

演示如何准备新的截面节点以进行编辑。

```csharp
Document doc = new Document();

// 空白文档有一个部分，该部分有一个正文，而正文又有一个段落。
// 我们可以通过向该段落添加文本、形状或表格等元素来向该文档添加内容。
Assert.AreEqual(NodeType.Section, doc.GetChild(NodeType.Any, 0, true).NodeType);
Assert.AreEqual(NodeType.Body, doc.Sections[0].GetChild(NodeType.Any, 0, true).NodeType);
Assert.AreEqual(NodeType.Paragraph, doc.Sections[0].Body.GetChild(NodeType.Any, 0, true).NodeType);

// 如果我们像这样添加一个新部分，它将没有主体或任何其他子节点。
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

* class [Section](../../section/)
* class [SectionCollection](../)
* 命名空间 [Aspose.Words](../../sectioncollection/)
* 部件 [Aspose.Words](../../../)


