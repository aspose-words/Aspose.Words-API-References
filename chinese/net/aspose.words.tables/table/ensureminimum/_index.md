---
title: Table.EnsureMinimum
linktitle: EnsureMinimum
articleTitle: EnsureMinimum
second_title: Aspose.Words for .NET
description: 发现 Table EnsureMinimum 方法，当表为空时轻松创建并附加一行，实现无缝数据管理。
type: docs
weight: 420
url: /zh/net/aspose.words.tables/table/ensureminimum/
---
## Table.EnsureMinimum method

如果表没有行，则创建并附加一行[`Row`](../../row/).

```csharp
public void EnsureMinimum()
```

## 例子

展示如何确保表节点包含我们需要添加内容的节点。

```csharp
Document doc = new Document();
Table table = new Table(doc);
doc.FirstSection.Body.AppendChild(table);

// 表格包含行，行包含单元格，单元格可能包含段落
// 具有典型元素，例如运行、形状，甚至其他表格。
// 我们的新表没有这些节点，并且我们不能向其中添加内容。
Assert.AreEqual(0, table.GetChildNodes(NodeType.Any, true).Count);

// 在表上调用“EnsureMinimum”方法将确保
// 表格至少有一行和一个带有空段落的单元格。
table.EnsureMinimum();
table.FirstRow.FirstCell.FirstParagraph.AppendChild(new Run(doc, "Hello world!"));
```

### 也可以看看

* class [Table](../)
* 命名空间 [Aspose.Words.Tables](../../../aspose.words.tables/)
* 部件 [Aspose.Words](../../../)
