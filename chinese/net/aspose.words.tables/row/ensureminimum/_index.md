---
title: Row.EnsureMinimum
linktitle: EnsureMinimum
articleTitle: EnsureMinimum
second_title: Aspose.Words for .NET
description: 发现 Row EnsureMinimum 方法，当不存在 Cell 时轻松创建并附加 Cell，增强数据结构管理。
type: docs
weight: 150
url: /zh/net/aspose.words.tables/row/ensureminimum/
---
## Row.EnsureMinimum method

如果[`Row`](../)没有单元格，创建并附加一个[`Cell`](../../cell/).

```csharp
public void EnsureMinimum()
```

## 例子

展示如何确保行节点包含我们开始向其添加内容所需的节点。

```csharp
Document doc = new Document();
Table table = new Table(doc);
doc.FirstSection.Body.AppendChild(table);
Row row = new Row(doc);
table.AppendChild(row);

// 行包含单元格，其中包含具有典型元素（例如运行、形状甚至其他表格）的段落。
// 我们的新行没有这些节点，并且我们不能向其中添加内容。
Assert.AreEqual(0, row.GetChildNodes(NodeType.Any, true).Count);

// 在表上调用“EnsureMinimum”方法将确保
// 表格中至少有一个单元格包含空段落。
row.EnsureMinimum();
row.FirstCell.FirstParagraph.AppendChild(new Run(doc, "Hello world!"));
```

### 也可以看看

* class [Row](../)
* 命名空间 [Aspose.Words.Tables](../../../aspose.words.tables/)
* 部件 [Aspose.Words](../../../)
