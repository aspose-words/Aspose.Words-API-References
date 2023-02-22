---
title: Class RowFormat
second_title: Aspose.Words for .NET API 参考
description: Aspose.Words.Tables.RowFormat 班级. 表示表格行的所有格式
type: docs
weight: 6030
url: /zh/net/aspose.words.tables/rowformat/
---
## RowFormat class

表示表格行的所有格式。

```csharp
public class RowFormat
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [AllowBreakAcrossPages](../../aspose.words.tables/rowformat/allowbreakacrosspages/) { get; set; } | 如果允许表格行中的文本跨分页符拆分，则为真。 |
| [Borders](../../aspose.words.tables/rowformat/borders/) { get; } | 获取行的默认单元格边框的集合。 |
| [HeadingFormat](../../aspose.words.tables/rowformat/headingformat/) { get; set; } | 当表格跨度超过一页时，如果该行作为表格标题在每一页上重复，则为真。 |
| [Height](../../aspose.words.tables/rowformat/height/) { get; set; } | 获取或设置表格行的高度，以磅为单位。 |
| [HeightRule](../../aspose.words.tables/rowformat/heightrule/) { get; set; } | 获取或设置表格行高确定规则 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [ClearFormatting](../../aspose.words.tables/rowformat/clearformatting/)() | 重置为默认行格式。 |

### 例子

显示如何修改表格行的格式。

```csharp
Document doc = new Document(MyDir + "Tables.docx");
Table table = doc.FirstSection.Body.Tables[0];

// 使用第一行的“RowFormat”属性设置修改整行外观的格式。
Row firstRow = table.FirstRow;
firstRow.RowFormat.Borders.LineStyle = LineStyle.None;
firstRow.RowFormat.HeightRule = HeightRule.Auto;
firstRow.RowFormat.AllowBreakAcrossPages = true;

doc.Save(ArtifactsDir + "Table.RowFormat.docx");
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

演示如何构建具有自定义边框的表格。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.StartTable();

// 为文档构建器设置表格格式选项
// 将它们应用于我们添加的每一行和单元格。
builder.ParagraphFormat.Alignment = ParagraphAlignment.Center;

builder.CellFormat.ClearFormatting();
builder.CellFormat.Width = 150;
builder.CellFormat.VerticalAlignment = CellVerticalAlignment.Center;
builder.CellFormat.Shading.BackgroundPatternColor = Color.GreenYellow;
builder.CellFormat.WrapText = false;
builder.CellFormat.FitText = true;

builder.RowFormat.ClearFormatting();
builder.RowFormat.HeightRule = HeightRule.Exactly;
builder.RowFormat.Height = 50;
builder.RowFormat.Borders.LineStyle = LineStyle.Engrave3D;
builder.RowFormat.Borders.Color = Color.Orange;

builder.InsertCell();
builder.Write("Row 1, Col 1");

builder.InsertCell();
builder.Write("Row 1, Col 2");
builder.EndRow();

// 更改格式会将其应用到当前单元格，
// 以及我们之后使用构建器创建的任何新单元格。
// 这不会影响我们之前添加的单元格。
builder.CellFormat.Shading.ClearFormatting();

builder.InsertCell();
builder.Write("Row 2, Col 1");

builder.InsertCell();
builder.Write("Row 2, Col 2");

builder.EndRow();

// 增加行高以适应垂直文本。
builder.InsertCell();
builder.RowFormat.Height = 150;
builder.CellFormat.Orientation = TextOrientation.Upward;
builder.Write("Row 3, Col 1");

builder.InsertCell();
builder.CellFormat.Orientation = TextOrientation.Downward;
builder.Write("Row 3, Col 2");

builder.EndRow();
builder.EndTable();

doc.Save(ArtifactsDir + "DocumentBuilder.InsertTable.docx");
```

### 也可以看看

* 命名空间 [Aspose.Words.Tables](../../aspose.words.tables/)
* 部件 [Aspose.Words](../../)


