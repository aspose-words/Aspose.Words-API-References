---
title: Table.AllowAutoFit
linktitle: AllowAutoFit
articleTitle: AllowAutoFit
second_title: Aspose.Words for .NET
description: 发现 Table AllowAutoFit 属性可以轻松调整 Microsoft Word 和 Aspose.Words 表格单元格的大小，从而增强文档的可读性和演示效果。
type: docs
weight: 50
url: /zh/net/aspose.words.tables/table/allowautofit/
---
## Table.AllowAutoFit property

允许 Microsoft Word 和 Aspose.Words 自动调整表格中单元格的大小以适应其内容。

```csharp
public bool AllowAutoFit { get; set; }
```

## 评论

默认值为`真的`。

## 例子

展示如何启用/禁用表格单元格自动调整大小。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.CellFormat.PreferredWidth = PreferredWidth.FromPoints(100);
builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
              "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

builder.InsertCell();
builder.CellFormat.PreferredWidth = PreferredWidth.Auto;
builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
              "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
builder.EndRow();
builder.EndTable();

// 将“AllowAutoFit”属性设置为“false”以使表格保持尺寸
// 所有行和单元格，如果它们太大而无法容纳，则截断内容。
// 将“AllowAutoFit”属性设置为“true”以允许表格改变其单元格的宽度和高度
// 以容纳其内容。
table.AllowAutoFit = allowAutoFit;

doc.Save(ArtifactsDir + "Table.AllowAutoFitOnTable.html");
```

### 也可以看看

* class [Table](../)
* 命名空间 [Aspose.Words.Tables](../../../aspose.words.tables/)
* 部件 [Aspose.Words](../../../)
