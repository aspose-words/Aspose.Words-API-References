---
title: PreferredWidth.FromPercent
linktitle: FromPercent
articleTitle: FromPercent
second_title: Aspose.Words for .NET
description: 探索 PreferredWidth FromPercent 方法，该方法会创建一个新实例，用于以百分比形式定义首选宽度。提升您的设计精度！
type: docs
weight: 20
url: /zh/net/aspose.words.tables/preferredwidth/frompercent/
---
## PreferredWidth.FromPercent method

一种创建方法，返回一个新实例，该实例表示以百分比指定的首选宽度。

```csharp
public static PreferredWidth FromPercent(double percent)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| percent | Double | 该值必须介于 0 到 100 之间。 |

## 例子

展示如何设置表格以自动适应页面宽度的 50%。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Cell #1");
builder.InsertCell();
builder.Write("Cell #2");
builder.InsertCell();
builder.Write("Cell #3");

table.PreferredWidth = PreferredWidth.FromPercent(50);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertTableWithPreferredWidth.docx");
```

展示如何设置表格单元格的首选宽度。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
Table table = builder.StartTable();

// 有两种方法可以将“PreferredWidth”类应用于表格单元格。
// 1 - 根据点设置绝对首选宽度：
builder.InsertCell();
builder.CellFormat.PreferredWidth = PreferredWidth.FromPoints(40);
builder.CellFormat.Shading.BackgroundPatternColor = Color.LightYellow;
builder.Writeln($"Cell with a width of {builder.CellFormat.PreferredWidth}.");

// 2 - 根据表格宽度的百分比设置相对首选宽度：
builder.InsertCell();
builder.CellFormat.PreferredWidth = PreferredWidth.FromPercent(20);
builder.CellFormat.Shading.BackgroundPatternColor = Color.LightBlue;
builder.Writeln($"Cell with a width of {builder.CellFormat.PreferredWidth}.");

builder.InsertCell();

// 未指定首选宽度的单元格将占用剩余的可用空间。
builder.CellFormat.PreferredWidth = PreferredWidth.Auto;

// “PreferredWidth”属性的每次配置都会创建一个新对象。
Assert.AreNotEqual(table.FirstRow.Cells[1].CellFormat.PreferredWidth.GetHashCode(),
    builder.CellFormat.PreferredWidth.GetHashCode());

builder.CellFormat.Shading.BackgroundPatternColor = Color.LightGreen;
builder.Writeln("Automatically sized cell.");

doc.Save(ArtifactsDir + "DocumentBuilder.InsertCellsWithPreferredWidths.docx");
```

### 也可以看看

* class [PreferredWidth](../)
* 命名空间 [Aspose.Words.Tables](../../../aspose.words.tables/)
* 部件 [Aspose.Words](../../../)
