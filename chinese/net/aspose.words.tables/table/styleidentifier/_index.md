---
title: Table.StyleIdentifier
second_title: Aspose.Words for .NET API 参考
description: Table 财产. 获取或设置应用于此表的表样式的区域设置独立样式标识符
type: docs
weight: 280
url: /zh/net/aspose.words.tables/table/styleidentifier/
---
## Table.StyleIdentifier property

获取或设置应用于此表的表样式的区域设置独立样式标识符。

```csharp
public StyleIdentifier StyleIdentifier { get; set; }
```

### 例子

演示如何在应用样式时构建新表格。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
Table table = builder.StartTable();

// 在设置任何表格格式之前，我们必须插入至少一行。
builder.InsertCell();

// 根据样式标识符设置使用的表格样式。
// 请注意，保存为 .doc 格式时并非所有表格样式都可用。
table.StyleIdentifier = StyleIdentifier.MediumShading1Accent1;

// 根据谓词将样式部分应用到表的特征，然后构建表。
table.StyleOptions =
    TableStyleOptions.FirstColumn | TableStyleOptions.RowBands | TableStyleOptions.FirstRow;
table.AutoFit(AutoFitBehavior.AutoFitToContents);

builder.Writeln("Item");
builder.CellFormat.RightPadding = 40;
builder.InsertCell();
builder.Writeln("Quantity (kg)");
builder.EndRow();

builder.InsertCell();
builder.Writeln("Apples");
builder.InsertCell();
builder.Writeln("20");
builder.EndRow();

builder.InsertCell();
builder.Writeln("Bananas");
builder.InsertCell();
builder.Writeln("40");
builder.EndRow();

builder.InsertCell();
builder.Writeln("Carrots");
builder.InsertCell();
builder.Writeln("50");
builder.EndRow();

doc.Save(ArtifactsDir + "DocumentBuilder.InsertTableWithStyle.docx");
```

### 也可以看看

* enum [StyleIdentifier](../../../aspose.words/styleidentifier/)
* class [Table](../)
* 命名空间 [Aspose.Words.Tables](../../table/)
* 部件 [Aspose.Words](../../../)


