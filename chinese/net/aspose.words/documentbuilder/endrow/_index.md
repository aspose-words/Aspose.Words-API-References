---
title: DocumentBuilder.EndRow
linktitle: EndRow
articleTitle: EndRow
second_title: Aspose.Words for .NET
description: 使用 DocumentBuilder 的 EndRow 方法轻松结束文档中的表格行。简化格式并增强文档清晰度！
type: docs
weight: 240
url: /zh/net/aspose.words/documentbuilder/endrow/
---
## DocumentBuilder.EndRow method

结束文档中的表格行。

```csharp
public Row EndRow()
```

### 返回值

刚刚完成的行节点。

## 评论

称呼`EndRow`结束表格行。如果您调用[`InsertCell`](../insertcell/)之后立即 ，然后表格继续在新的一行上。

使用[`RowFormat`](../rowformat/)属性来指定行格式。

## 例子

显示如何垂直合并表格单元格。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 在第一行的第一列插入一个单元格。
// 此单元格将是垂直合并单元格范围内的第一个单元格。
builder.InsertCell();
builder.CellFormat.VerticalMerge = CellMerge.First;
builder.Write("Text in merged cells.");

// 在第一行的第二列插入一个单元格，然后结束该行。
// 另外，配置构建器以禁用创建的单元格中的垂直合并。
builder.InsertCell();
builder.CellFormat.VerticalMerge = CellMerge.None;
builder.Write("Text in unmerged cell.");
builder.EndRow();

 // 在第二行的第一列插入一个单元格。
// 我们不会添加文本内容，而是将此单元格与我们直接在上面添加的第一个单元格合并。
builder.InsertCell();
builder.CellFormat.VerticalMerge = CellMerge.Previous;

// 在第二行第二列插入另一个独立单元格。
builder.InsertCell();
builder.CellFormat.VerticalMerge = CellMerge.None;
builder.Write("Text in unmerged cell.");
builder.EndRow();
builder.EndTable();

doc.Save(ArtifactsDir + "CellFormat.VerticalMerge.docx");
```

展示如何构建格式化的 2x2 表。

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
// 到其光标所在的当前行/单元格以及它创建的任何新行/单元格。
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

// 先前添加的行和单元格不会因构建器格式的更改而受到追溯影响。
Assert.AreEqual(0, table.Rows[0].RowFormat.Height);
Assert.AreEqual(HeightRule.Auto, table.Rows[0].RowFormat.HeightRule);
Assert.AreEqual(100, table.Rows[1].RowFormat.Height);
Assert.AreEqual(HeightRule.Exactly, table.Rows[1].RowFormat.HeightRule);
Assert.AreEqual(TextOrientation.Upward, table.Rows[1].Cells[0].CellFormat.Orientation);
Assert.AreEqual(TextOrientation.Downward, table.Rows[1].Cells[1].CellFormat.Orientation);

doc.Save(ArtifactsDir + "DocumentBuilder.BuildTable.docx");
```

展示如何构建具有自定义边框的表格。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.StartTable();

// 为文档生成器设置表格格式选项
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

// 更改格式将应用于当前单元格，
// 以及我们随后使用构建器创建的任何新单元格。
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

* class [Row](../../../aspose.words.tables/row/)
* class [DocumentBuilder](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
