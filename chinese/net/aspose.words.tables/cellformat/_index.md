---
title: CellFormat Class
linktitle: CellFormat
articleTitle: CellFormat
second_title: 用于 .NET 的 Aspose.Words
description: Aspose.Words.Tables.CellFormat 班级. 表示表格单元格的所有格式 在 C#.
type: docs
weight: 6260
url: /zh/net/aspose.words.tables/cellformat/
---
## CellFormat class

表示表格单元格的所有格式。

要了解更多信息，请访问[使用表格](https://docs.aspose.com/words/net/working-with-tables/)文档文章。

```csharp
public class CellFormat
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [Borders](../../aspose.words.tables/cellformat/borders/) { get; } | 获取单元格边框的集合。 |
| [BottomPadding](../../aspose.words.tables/cellformat/bottompadding/) { get; set; } | 返回或设置要在单元格内容下方添加的空间量（以磅为单位）。 |
| [FitText](../../aspose.words.tables/cellformat/fittext/) { get; set; } | 如果`真的` ，适合单元格中的文本，将每个段落压缩到单元格的宽度。 |
| [HorizontalMerge](../../aspose.words.tables/cellformat/horizontalmerge/) { get; set; } | 指定单元格如何与行中的其他单元格水平合并。 |
| [LeftPadding](../../aspose.words.tables/cellformat/leftpadding/) { get; set; } | 返回或设置要添加到单元格内容左侧的空间量（以磅为单位）。 |
| [Orientation](../../aspose.words.tables/cellformat/orientation/) { get; set; } | 返回或设置表格单元格中文本的方向。 |
| [PreferredWidth](../../aspose.words.tables/cellformat/preferredwidth/) { get; set; } | 返回或设置单元格的首选宽度。 |
| [RightPadding](../../aspose.words.tables/cellformat/rightpadding/) { get; set; } | 返回或设置要添加到单元格内容右侧的空间量（以磅为单位）。 |
| [Shading](../../aspose.words.tables/cellformat/shading/) { get; } | 返回一个[`Shading`](../../aspose.words/shading/)引用单元格着色格式的对象。 |
| [TopPadding](../../aspose.words.tables/cellformat/toppadding/) { get; set; } | 返回或设置要在单元格内容上方添加的空间量（以磅为单位）。 |
| [VerticalAlignment](../../aspose.words.tables/cellformat/verticalalignment/) { get; set; } | 返回或设置单元格中文本的垂直对齐方式。 |
| [VerticalMerge](../../aspose.words.tables/cellformat/verticalmerge/) { get; set; } | 指定单元格如何与其他单元格垂直合并。 |
| [Width](../../aspose.words.tables/cellformat/width/) { get; set; } | 获取单元格的宽度（以磅为单位）。 |
| [WrapText](../../aspose.words.tables/cellformat/wraptext/) { get; set; } | 如果`真的` ，单元格文本换行。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [ClearFormatting](../../aspose.words.tables/cellformat/clearformatting/)() | 重置为默认单元格格式。不改变单元格的宽度。 |
| [SetPaddings](../../aspose.words.tables/cellformat/setpaddings/)(*double, double, double, double*) | 设置添加到单元格内容的左侧/顶部/右侧/底部的空间量（以磅为单位）。 |

## 例子

演示如何修改表格单元格的格式。

```csharp
Document doc = new Document(MyDir + "Tables.docx");
Table table = doc.FirstSection.Body.Tables[0];
Cell firstCell = table.FirstRow.FirstCell;

// 使用单元格的“CellFormat”属性来设置修改该单元格外观的格式。
firstCell.CellFormat.Width = 30;
firstCell.CellFormat.Orientation = TextOrientation.Downward;
firstCell.CellFormat.Shading.ForegroundPatternColor = Color.LightGreen;

doc.Save(ArtifactsDir + "Table.CellFormat.docx");
```

演示如何修改表中行和单元格的格式。

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
// 该行中所有单元格的内容。
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

// 为文档生成器设置表格格式选项
// 将它们应用到我们添加的每一行和单元格。
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
// 以及我们随后使用构建器创建的任何新单元格。
// 这不会影响我们之前添加的单元格。
builder.CellFormat.Shading.ClearFormatting();

builder.InsertCell();
builder.Write("Row 2, Col 1");

builder.InsertCell();
builder.Write("Row 2, Col 2");

builder.EndRow();

// 增加行高以适合垂直文本。
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
