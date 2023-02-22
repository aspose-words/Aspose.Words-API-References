---
title: DocumentBuilder.StartTable
second_title: Aspose.Words for .NET API 参考
description: DocumentBuilder 方法. 在文档中开始一个表
type: docs
weight: 610
url: /zh/net/aspose.words/documentbuilder/starttable/
---
## DocumentBuilder.StartTable method

在文档中开始一个表。

```csharp
public Table StartTable()
```

### 返回值

刚刚创建的表节点。

### 评论

下一个调用方法是[`InsertCell`](../insertcell/).

此方法在单元格内调用时会启动一个嵌套表。

### 例子

显示如何使用文档构建器格式化单元格。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Row 1, cell 1.");

// 插入第二个单元格，然后配置单元格文本填充选项。
// 构建器将在其当前单元格中应用这些设置，然后创建任何新单元格。
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

// 第一个单元格不受填充重新配置的影响，仍然保持默认值。
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

// 第一个单元格仍将在输出文档中增长以匹配其相邻单元格的大小。
doc.Save(ArtifactsDir + "DocumentBuilder.SetCellFormatting.docx");
```

展示如何构建格式化的 2x2 表格。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.CellFormat.VerticalAlignment = CellVerticalAlignment.Center;
builder.Write("Row 1, cell 1.");
builder.InsertCell();
builder.Write("Row 1, cell 2.");
builder.EndRow();

// 在构建表格时，文档构建器将应用其当前的 RowFormat/CellFormat 属性值
// 到其光标所在的当前行/单元格以及创建它们时的任何新行/单元格。
Assert.AreEqual(CellVerticalAlignment.Center, table.Rows[0].Cells[0].CellFormat.VerticalAlignment);
Assert.AreEqual(CellVerticalAlignment.Center, table.Rows[0].Cells[1].CellFormat.VerticalAlignment);

builder.InsertCell();
builder.RowFormat.Height = 100;
builder.RowFormat.HeightRule = HeightRule.Exactly;
builder.CellFormat.Orientation = TextOrientation.Upward;
builder.Write("Row 2, cell 1.");
builder.InsertCell();
builder.CellFormat.Orientation = TextOrientation.Downward;
builder.Write("Row 2, cell 2.");
builder.EndRow();
builder.EndTable();

// 先前添加的行和单元格不受构建器格式更改的追溯影响。
Assert.AreEqual(0, table.Rows[0].RowFormat.Height);
Assert.AreEqual(HeightRule.Auto, table.Rows[0].RowFormat.HeightRule);
Assert.AreEqual(100, table.Rows[1].RowFormat.Height);
Assert.AreEqual(HeightRule.Exactly, table.Rows[1].RowFormat.HeightRule);
Assert.AreEqual(TextOrientation.Upward, table.Rows[1].Cells[0].CellFormat.Orientation);
Assert.AreEqual(TextOrientation.Downward, table.Rows[1].Cells[1].CellFormat.Orientation);

doc.Save(ArtifactsDir + "DocumentBuilder.BuildTable.docx");
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

* class [Table](../../../aspose.words.tables/table/)
* class [DocumentBuilder](../)
* 命名空间 [Aspose.Words](../../documentbuilder/)
* 部件 [Aspose.Words](../../../)


