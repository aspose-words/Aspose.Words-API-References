---
title: Cell.EnsureMinimum
linktitle: EnsureMinimum
articleTitle: EnsureMinimum
second_title: Aspose.Words for .NET
description: 使用 EnsureMinimum 方法优化单元格结构，即使最后一个子元素不是段落，也能轻松添加段落。提升文档的清晰度！
type: docs
weight: 160
url: /zh/net/aspose.words.tables/cell/ensureminimum/
---
## Cell.EnsureMinimum method

如果最后一个子项不是段落，则创建并附加一个空段落。

```csharp
public void EnsureMinimum()
```

## 例子

展示如何确保单元节点包含我们开始向其添加内容所需的节点。

```csharp
Document doc = new Document();
Table table = new Table(doc);
doc.FirstSection.Body.AppendChild(table);
Row row = new Row(doc);
table.AppendChild(row);
Cell cell = new Cell(doc);
row.AppendChild(cell);

// 单元格可能包含具有典型元素的段落，例如运行、形状甚至其他表格。
// 我们的新单元格没有任何段落，在此之前我们无法向其中添加运行和形状节点等内容。
Assert.AreEqual(0, cell.GetChildNodes(NodeType.Any, true).Count);

// 在单元格上调用“EnsureMinimum”方法将确保
// 单元格至少有一个空段落，我们可以向其中添加内容。
cell.EnsureMinimum();
cell.FirstParagraph.AppendChild(new Run(doc, "Hello world!"));
```

### 也可以看看

* class [Cell](../)
* 命名空间 [Aspose.Words.Tables](../../../aspose.words.tables/)
* 部件 [Aspose.Words](../../../)
