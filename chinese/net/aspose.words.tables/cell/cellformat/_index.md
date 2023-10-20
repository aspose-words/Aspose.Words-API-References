---
title: Cell.CellFormat
linktitle: CellFormat
articleTitle: CellFormat
second_title: 用于 .NET 的 Aspose.Words
description: Cell CellFormat 财产. 提供对单元格格式属性的访问 在 C#.
type: docs
weight: 20
url: /zh/net/aspose.words.tables/cell/cellformat/
---
## Cell.CellFormat property

提供对单元格格式属性的访问。

```csharp
public CellFormat CellFormat { get; }
```

## 例子

显示如何修改表格单元格的格式。

```csharp
Document doc = new Document(MyDir + "Tables.docx");
Table table = doc.FirstSection.Body.Tables[0];
Cell firstCell = table.FirstRow.FirstCell;

// 使用单元格的“CellFormat”属性设置修改该单元格外观的格式。
firstCell.CellFormat.Width = 30;
firstCell.CellFormat.Orientation = TextOrientation.Downward;
firstCell.CellFormat.Shading.ForegroundPatternColor = Color.LightGreen;

doc.Save(ArtifactsDir + "Table.CellFormat.docx");
```

显示如何将两个表中的行合并为一个。

```csharp
Document doc = new Document(MyDir + "Tables.docx");

// 下面是从文档中获取表格的两种方法。
// 1 - 来自 Body 节点的“Tables”集合：
Table firstTable = doc.FirstSection.Body.Tables[0];

// 2 - 使用“GetChild”方法：
Table secondTable = (Table)doc.GetChild(NodeType.Table, 1, true);

// 将当前表中的所有行追加到下一个表中。
while (secondTable.HasChildNodes)
    firstTable.Rows.Add(secondTable.FirstRow);

// 删除空表容器。
secondTable.Remove();

doc.Save(ArtifactsDir + "Table.CombineTables.docx");
```

显示如何修改表格中行和单元格的格式。

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

// 使用第一行的“RowFormat”属性修改格式
// 此行中所有单元格的内容。
RowFormat rowFormat = table.FirstRow.RowFormat;
rowFormat.Height = 25;
rowFormat.Borders[BorderType.Bottom].Color = Color.Red;

// 使用最后一行中第一个单元格的“CellFormat”属性来修改该单元格内容的格式。
CellFormat cellFormat = table.LastRow.FirstCell.CellFormat;
cellFormat.Width = 100;
cellFormat.Shading.BackgroundPatternColor = Color.Orange;

doc.Save(ArtifactsDir + "Table.RowCellFormat.docx");
```

### 也可以看看

* class [CellFormat](../../cellformat/)
* class [Cell](../)
* 命名空间 [Aspose.Words.Tables](../../../aspose.words.tables/)
* 部件 [Aspose.Words](../../../)
