---
title: Table.ConvertToHorizontallyMergedCells
linktitle: ConvertToHorizontallyMergedCells
articleTitle: ConvertToHorizontallyMergedCells
second_title: Aspose.Words for .NET
description: 了解 ConvertToHorizontallyMergedCells 方法如何将宽合并单元格转换为水平合并单元格，从而增强数据组织。
type: docs
weight: 410
url: /zh/net/aspose.words.tables/table/converttohorizontallymergedcells/
---
## Table.ConvertToHorizontallyMergedCells method

将按宽度水平合并的单元格转换为按[`HorizontalMerge`](../../cellformat/horizontalmerge/).

```csharp
public void ConvertToHorizontallyMergedCells()
```

## 评论

表格单元格可以使用合并标志进行水平合并[`HorizontalMerge`](../../cellformat/horizontalmerge/)或使用单元格宽度[`Width`](../../cellformat/width/)。

当表格单元格按 width 属性合并时[`HorizontalMerge`](../../cellformat/horizontalmerge/)是没有意义的，但有时合并标志是更方便的方式。

使用此方法将按宽度水平合并的表格单元格转换为按合并标志合并的单元格。

## 例子

展示如何将按宽度水平合并的单元格转换为通过 CellFormat.HorizontalMerge 合并的单元格。

```csharp
Document doc = new Document(MyDir + "Table with merged cells.docx");

// Microsoft Word 不再写入合并标志，而是通过宽度定义合并单元格。
// Aspose.Words 默认一行只定义 5 个单元格，并且没有一个单元格具有水平合并标志，
// 即使在水平合并发生之前该行中有 7 个单元格。
Table table = doc.FirstSection.Body.Tables[0];
Row row = table.Rows[0];

Assert.AreEqual(5, row.Cells.Count);
Assert.True(row.Cells.All(c => ((Cell)c).CellFormat.HorizontalMerge == CellMerge.None));

// 使用“ConvertToHorizontallyMergedCells”方法将单元格转换为水平合并
// 按其宽度与通过标志水平合并的单元格相合并。
// 现在，我们有 7 个单元格，其中一些具有水平合并值。
table.ConvertToHorizontallyMergedCells();
row = table.Rows[0];

Assert.AreEqual(7, row.Cells.Count);

Assert.AreEqual(CellMerge.None, row.Cells[0].CellFormat.HorizontalMerge);
Assert.AreEqual(CellMerge.First, row.Cells[1].CellFormat.HorizontalMerge);
Assert.AreEqual(CellMerge.Previous, row.Cells[2].CellFormat.HorizontalMerge);
Assert.AreEqual(CellMerge.None, row.Cells[3].CellFormat.HorizontalMerge);
Assert.AreEqual(CellMerge.First, row.Cells[4].CellFormat.HorizontalMerge);
Assert.AreEqual(CellMerge.Previous, row.Cells[5].CellFormat.HorizontalMerge);
Assert.AreEqual(CellMerge.None, row.Cells[6].CellFormat.HorizontalMerge);
```

### 也可以看看

* class [Table](../)
* 命名空间 [Aspose.Words.Tables](../../../aspose.words.tables/)
* 部件 [Aspose.Words](../../../)
