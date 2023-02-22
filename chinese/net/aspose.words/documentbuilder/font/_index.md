---
title: DocumentBuilder.Font
second_title: Aspose.Words for .NET API 参考
description: DocumentBuilder 财产. 返回一个表示当前字体格式属性的对象
type: docs
weight: 90
url: /zh/net/aspose.words/documentbuilder/font/
---
## DocumentBuilder.Font property

返回一个表示当前字体格式属性的对象。

```csharp
public Font Font { get; }
```

### 评论

利用 **字体**访问和修改字体格式属性。

在插入文本之前指定字体格式。

### 例子

演示如何将由边框包围的字符串插入到文档中。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Border.Color = Color.Green;
builder.Font.Border.LineWidth = 2.5d;
builder.Font.Border.LineStyle = LineStyle.DashDotStroker;

builder.Write("Text surrounded by green border.");

doc.Save(ArtifactsDir + "Border.FontBorder.docx");
```

展示如何使用 DocumentBuilder 创建格式化表格。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
table.LeftIndent = 20;

// 为文本和表格外观设置一些格式选项。
builder.RowFormat.Height = 40;
builder.RowFormat.HeightRule = HeightRule.AtLeast;
builder.CellFormat.Shading.BackgroundPatternColor = Color.FromArgb(198, 217, 241);

builder.ParagraphFormat.Alignment = ParagraphAlignment.Center;
builder.Font.Size = 16;
builder.Font.Name = "Arial";
builder.Font.Bold = true;

// 在文档构建器中配置格式选项将应用它们
// 到其光标所在的当前单元格/行，
// 以及使用该构建器创建的任何新单元格和行。
builder.Write("Header Row,\n Cell 1");
builder.InsertCell();
builder.Write("Header Row,\n Cell 2");
builder.InsertCell();
builder.Write("Header Row,\n Cell 3");
builder.EndRow();

// 为我们即将创建的新行和单元格重新配置构建器的格式化对象。
// 构建器不会将这些应用到已经创建的第一行，以便它将作为标题行突出。
builder.CellFormat.Shading.BackgroundPatternColor = Color.White;
builder.CellFormat.VerticalAlignment = CellVerticalAlignment.Center;
builder.RowFormat.Height = 30;
builder.RowFormat.HeightRule = HeightRule.Auto;
builder.InsertCell();
builder.Font.Size = 12;
builder.Font.Bold = false;

builder.Write("Row 1, Cell 1.");
builder.InsertCell();
builder.Write("Row 1, Cell 2.");
builder.InsertCell();
builder.Write("Row 1, Cell 3.");
builder.EndRow();
builder.InsertCell();
builder.Write("Row 2, Cell 1.");
builder.InsertCell();
builder.Write("Row 2, Cell 2.");
builder.InsertCell();
builder.Write("Row 2, Cell 3.");
builder.EndRow();
builder.EndTable();

doc.Save(ArtifactsDir + "DocumentBuilder.CreateFormattedTable.docx");
```

### 也可以看看

* class [Font](../../font/)
* class [DocumentBuilder](../)
* 命名空间 [Aspose.Words](../../documentbuilder/)
* 部件 [Aspose.Words](../../../)


