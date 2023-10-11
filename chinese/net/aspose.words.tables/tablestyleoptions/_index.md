---
title: Enum TableStyleOptions
second_title: Aspose.Words for .NET API 参考
description: Aspose.Words.Tables.TableStyleOptions 枚举. 指定如何将表格样式应用于表格
type: docs
weight: 6370
url: /zh/net/aspose.words.tables/tablestyleoptions/
---
## TableStyleOptions enumeration

指定如何将表格样式应用于表格。

```csharp
[Flags]
public enum TableStyleOptions
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| None | `0` | 未应用表格样式格式。 |
| FirstRow | `20` | 应用第一行条件格式。 |
| LastRow | `40` | 应用最后一行条件格式。 |
| FirstColumn | `80` | 应用 1 个第一列条件格式。 |
| LastColumn | `100` | 应用最后一列条件格式。 |
| RowBands | `200` | 应用行带条件格式。 |
| ColumnBands | `400` | 应用列带条件格式。 |
| Default2003 | `600` | 应用行和列条带。这是 Microsoft Word 对于 DOC、WML 和 RTF 等旧格式的默认设置。 |
| Default | `2A0` | 这是 Microsoft Word 默认值。 |

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

* property [StyleOptions](../table/styleoptions/)
* 命名空间 [Aspose.Words.Tables](../../aspose.words.tables/)
* 部件 [Aspose.Words](../../)


