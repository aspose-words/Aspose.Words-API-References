---
title: CellFormat.Width
linktitle: Width
articleTitle: Width
second_title: 用于 .NET 的 Aspose.Words
description: CellFormat Width 财产. 获取单元格的宽度以磅为单位 在 C#.
type: docs
weight: 130
url: /zh/net/aspose.words.tables/cellformat/width/
---
## CellFormat.Width property

获取单元格的宽度（以磅为单位）。

```csharp
public double Width { get; set; }
```

## 评论

宽度由 Aspose.Words 在文档加载和保存时计算。 目前，并非支持表格、单元格和文档属性的所有组合。 对于某些文档，返回的值可能不准确。 它可能不完全匹配在 MS Word 中打开文档时由 MS Word 计算的单元格宽度。

不建议设置此属性。 不能保证单元格实际上具有设置的宽度。 可以调整宽度以适应自动调整表格布局中的单元格内容。 其他行中的单元格可能具有冲突的宽度设置。 可以调整表格大小以适合容器或满足表格宽度设置。 考虑使用[`PreferredWidth`](../preferredwidth/)用于设置单元格宽度。 设置此属性集[`PreferredWidth`](../preferredwidth/)自版本 15.8. 起隐式

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

* class [CellFormat](../)
* 命名空间 [Aspose.Words.Tables](../../../aspose.words.tables/)
* 部件 [Aspose.Words](../../../)
