---
title: RowFormat.HeadingFormat
linktitle: HeadingFormat
articleTitle: HeadingFormat
second_title: 用于 .NET 的 Aspose.Words
description: RowFormat HeadingFormat 财产. 如果当表格跨越一页以上时该行作为表格标题在每一页上重复则为 True 在 C#.
type: docs
weight: 30
url: /zh/net/aspose.words.tables/rowformat/headingformat/
---
## RowFormat.HeadingFormat property

如果当表格跨越一页以上时，该行作为表格标题在每一页上重复，则为 True。

```csharp
public bool HeadingFormat { get; set; }
```

## 例子

演示如何构建一个表，其中的行在每页上重复。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();

// 当“HeadingFormat”标志设置为“true”时插入的任何行
// 将显示在其跨越的每个页面的表格顶部。
builder.RowFormat.HeadingFormat = true;
builder.ParagraphFormat.Alignment = ParagraphAlignment.Center;
builder.CellFormat.Width = 100;
builder.InsertCell();
builder.Write("Heading row 1");
builder.EndRow();
builder.InsertCell();
builder.Write("Heading row 2");
builder.EndRow();

builder.CellFormat.Width = 50;
builder.ParagraphFormat.ClearFormatting();
builder.RowFormat.HeadingFormat = false;

// 添加足够的行以使表格跨越两页。
for (int i = 0; i < 50; i++)
{
    builder.InsertCell();
    builder.Write($"Row {table.Rows.Count}, column 1.");
    builder.InsertCell();
    builder.Write($"Row {table.Rows.Count}, column 2.");
    builder.EndRow();
}

doc.Save(ArtifactsDir + "DocumentBuilder.InsertTableSetHeadingRow.docx");
```

### 也可以看看

* class [RowFormat](../)
* 命名空间 [Aspose.Words.Tables](../../../aspose.words.tables/)
* 部件 [Aspose.Words](../../../)
