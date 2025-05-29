---
title: Table.AutoFit
linktitle: AutoFit
articleTitle: AutoFit
second_title: Aspose.Words for .NET
description: 探索表格自动调整方法，轻松调整表格和单元格大小，实现最佳布局。轻松提升文档的呈现效果！
type: docs
weight: 380
url: /zh/net/aspose.words.tables/table/autofit/
---
## Table.AutoFit method

根据指定的自动适应行为调整表格和单元格的大小。

```csharp
public void AutoFit(AutoFitBehavior behavior)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| behavior | AutoFitBehavior | 指定如何自动适应表格。 |

## 评论

此方法模拟了 Microsoft Word 中表格“自动调整”菜单中的可用命令。 可用的命令包括“自动调整至内容”、“自动调整至窗口”和“固定列宽”。在 Microsoft Word 中，这些命令会设置相关的表格属性，然后更新表格布局，Aspose.Words 也会为您执行相同的操作。

## 例子

展示如何在应用样式的同时构建新表。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
Table table = builder.StartTable();

// 在设置任何表格格式之前，我们必须插入至少一行。
builder.InsertCell();

// 根据样式标识符设置使用的表格样式。
// 请注意，保存为 .doc 格式时并非所有表格样式都可用。
table.StyleIdentifier = StyleIdentifier.MediumShading1Accent1;

// 根据谓词将样式部分应用于表的特征，然后构建表。
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

* enum [AutoFitBehavior](../../autofitbehavior/)
* class [Table](../)
* 命名空间 [Aspose.Words.Tables](../../../aspose.words.tables/)
* 部件 [Aspose.Words](../../../)
