---
title: PreferredWidth.FromPoints
second_title: Aspose.Words for .NET API 参考
description: PreferredWidth 方法. 一种创建方法返回一个新实例该实例表示使用多个点指定的首选宽度
type: docs
weight: 30
url: /zh/net/aspose.words.tables/preferredwidth/frompoints/
---
## PreferredWidth.FromPoints method

一种创建方法，返回一个新实例，该实例表示使用多个点指定的首选宽度。

```csharp
public static PreferredWidth FromPoints(double points)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| points | Double | 该值必须介于 0 到 22 英寸（22 * 72 点）之间。 |

### 例子

演示如何在指定单元格的首选宽度时使用单位转换工具。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.CellFormat.PreferredWidth = PreferredWidth.FromPoints(ConvertUtil.InchToPoint(3));
builder.InsertCell();

Assert.AreEqual(216.0d, table.FirstRow.FirstCell.CellFormat.PreferredWidth.Value);
```

演示如何设置表格单元格的首选宽度。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
Table table = builder.StartTable();

// 有两种方法将“PreferredWidth”类应用于表格单元格。
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

// “PreferredWidth”属性的每个配置都会创建一个新对象。
Assert.AreNotEqual(table.FirstRow.Cells[1].CellFormat.PreferredWidth.GetHashCode(),
    builder.CellFormat.PreferredWidth.GetHashCode());

builder.CellFormat.Shading.BackgroundPatternColor = Color.LightGreen;
builder.Writeln("Automatically sized cell.");

doc.Save(ArtifactsDir + "DocumentBuilder.InsertCellsWithPreferredWidths.docx");
```

### 也可以看看

* class [PreferredWidth](../)
* 命名空间 [Aspose.Words.Tables](../../preferredwidth/)
* 部件 [Aspose.Words](../../../)


