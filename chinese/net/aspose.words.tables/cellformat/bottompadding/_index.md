---
title: CellFormat.BottomPadding
linktitle: BottomPadding
articleTitle: BottomPadding
second_title: 用于 .NET 的 Aspose.Words
description: CellFormat BottomPadding 财产. 返回或设置要在单元格内容下方添加的空间量以磅为单位 在 C#.
type: docs
weight: 20
url: /zh/net/aspose.words.tables/cellformat/bottompadding/
---
## CellFormat.BottomPadding property

返回或设置要在单元格内容下方添加的空间量（以磅为单位）。

```csharp
public double BottomPadding { get; set; }
```

## 例子

演示如何使用文档生成器设置单元格格式。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Row 1, cell 1.");

// 插入第二个单元格，然后配置单元格文本填充选项。
// 构建器将在其当前单元格应用这些设置，然后创建任何新单元格。
builder.InsertCell();

CellFormat cellFormat = builder.CellFormat;
cellFormat.Width = 250;
cellFormat.LeftPadding = 30;
cellFormat.RightPadding = 30;
cellFormat.TopPadding = 30;
cellFormat.BottomPadding = 30;

builder.Write("Row 1, cell 2.");
builder.EndRow();
builder.EndTable();

// 第一个单元格不受填充重新配置的影响，并且仍然保留默认值。
Assert.AreEqual(0.0d, table.FirstRow.Cells[0].CellFormat.Width);
Assert.AreEqual(5.4d, table.FirstRow.Cells[0].CellFormat.LeftPadding);
Assert.AreEqual(5.4d, table.FirstRow.Cells[0].CellFormat.RightPadding);
Assert.AreEqual(0.0d, table.FirstRow.Cells[0].CellFormat.TopPadding);
Assert.AreEqual(0.0d, table.FirstRow.Cells[0].CellFormat.BottomPadding);

Assert.AreEqual(250.0d, table.FirstRow.Cells[1].CellFormat.Width);
Assert.AreEqual(30.0d, table.FirstRow.Cells[1].CellFormat.LeftPadding);
Assert.AreEqual(30.0d, table.FirstRow.Cells[1].CellFormat.RightPadding);
Assert.AreEqual(30.0d, table.FirstRow.Cells[1].CellFormat.TopPadding);
Assert.AreEqual(30.0d, table.FirstRow.Cells[1].CellFormat.BottomPadding);

// 第一个单元格仍将在输出文档中增长，以匹配其相邻单元格的大小。
doc.Save(ArtifactsDir + "DocumentBuilder.SetCellFormatting.docx");
```

### 也可以看看

* class [CellFormat](../)
* 命名空间 [Aspose.Words.Tables](../../../aspose.words.tables/)
* 部件 [Aspose.Words](../../../)
