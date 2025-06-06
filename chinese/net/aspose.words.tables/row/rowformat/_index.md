---
title: Row.RowFormat
linktitle: RowFormat
articleTitle: RowFormat
second_title: Aspose.Words for .NET
description: 发现 RowRowFormat 属性可轻松访问可自定义的行格式选项，毫不费力地增强数据呈现。
type: docs
weight: 110
url: /zh/net/aspose.words.tables/row/rowformat/
---
## Row.RowFormat property

提供对行的格式属性的访问。

```csharp
public RowFormat RowFormat { get; }
```

## 例子

展示如何修改表格行的格式。

```csharp
Document doc = new Document(MyDir + "Tables.docx");
Table table = doc.FirstSection.Body.Tables[0];

// 使用第一行的“RowFormat”属性来设置修改整行外观的格式。
Row firstRow = table.FirstRow;
firstRow.RowFormat.Borders.LineStyle = LineStyle.None;
firstRow.RowFormat.HeightRule = HeightRule.Auto;
firstRow.RowFormat.AllowBreakAcrossPages = true;

doc.Save(ArtifactsDir + "Table.RowFormat.docx");
```

展示如何修改表中行和单元格的格式。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("City");
builder.InsertCell();
builder.Write("Country");
builder.EndRow();
builder.InsertCell();
builder.Write("London");
builder.InsertCell();
builder.Write("U.K.");
builder.EndTable();

// 使用第一行的“RowFormat”属性来修改格式
// 此行中所有单元格的内容。
RowFormat rowFormat = table.FirstRow.RowFormat;
rowFormat.Height = 25;
rowFormat.Borders[BorderType.Bottom].Color = Color.Red;

// 使用最后一行第一个单元格的“CellFormat”属性来修改该单元格内容的格式。
CellFormat cellFormat = table.LastRow.FirstCell.CellFormat;
cellFormat.Width = 100;
cellFormat.Shading.BackgroundPatternColor = Color.Orange;

doc.Save(ArtifactsDir + "Table.RowCellFormat.docx");
```

### 也可以看看

* class [RowFormat](../../rowformat/)
* class [Row](../)
* 命名空间 [Aspose.Words.Tables](../../../aspose.words.tables/)
* 部件 [Aspose.Words](../../../)
