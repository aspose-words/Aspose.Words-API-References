---
title: DocumentBuilder.ParagraphFormat
linktitle: ParagraphFormat
articleTitle: ParagraphFormat
second_title: Aspose.Words for .NET
description: 探索 DocumentBuilder 的 ParagraphFormat 属性以访问和自定义基本段落格式功能，从而增强文档样式。
type: docs
weight: 170
url: /zh/net/aspose.words/documentbuilder/paragraphformat/
---
## DocumentBuilder.ParagraphFormat property

返回表示当前段落格式属性的对象。

```csharp
public ParagraphFormat ParagraphFormat { get; }
```

## 例子

展示如何使用 DocumentBuilder 创建格式化的表格。

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

// 在文档生成器中配置格式选项将应用它们
// 到光标所在的当前单元格/行，
// 以及使用该构建器创建的任何新单元格和行。
builder.Write("Header Row,\n Cell 1");
builder.InsertCell();
builder.Write("Header Row,\n Cell 2");
builder.InsertCell();
builder.Write("Header Row,\n Cell 3");
builder.EndRow();

// 为我们即将创建的新行和新单元格重新配置构建器的格式化对象。
// 构建器不会将这些应用到已创建的第一行，以便它将作为标题行突出显示。
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

* class [ParagraphFormat](../../paragraphformat/)
* class [DocumentBuilder](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
