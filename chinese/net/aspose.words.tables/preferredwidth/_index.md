---
title: Class PreferredWidth
second_title: Aspose.Words for .NET API 参考
description: Aspose.Words.Tables.PreferredWidth 班级. 表示一个值及其度量单位用于指定表格或单元格的首选宽度
type: docs
weight: 5990
url: /zh/net/aspose.words.tables/preferredwidth/
---
## PreferredWidth class

表示一个值及其度量单位，用于指定表格或单元格的首选宽度。

```csharp
public sealed class PreferredWidth
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [Type](../../aspose.words.tables/preferredwidth/type/) { get; } | 获取用于此首选宽度值的测量单位。 |
| [Value](../../aspose.words.tables/preferredwidth/value/) { get; } | 获取首选宽度值。计量单位在[`Type`](./type/)属性. |

## 方法

| 姓名 | 描述 |
| --- | --- |
| static [FromPercent](../../aspose.words.tables/preferredwidth/frompercent/)(double) | 一种创建方法，它返回一个新实例，该实例表示指定为百分比的首选宽度。 |
| static [FromPoints](../../aspose.words.tables/preferredwidth/frompoints/)(double) | 一种创建方法，它返回一个新实例，该实例表示使用点数指定的首选宽度。 |
| override [Equals](../../aspose.words.tables/preferredwidth/equals/#equals_1)(object) | 确定指定对象的值是否与当前对象相等。 |
| [Equals](../../aspose.words.tables/preferredwidth/equals/#equals)(PreferredWidth) | 确定指定的 PreferredWidth 在值上是否等于当前 PreferredWidth。 |
| override [GetHashCode](../../aspose.words.tables/preferredwidth/gethashcode/)() | 用作此类型的哈希函数。 |
| override [ToString](../../aspose.words.tables/preferredwidth/tostring/)() | 返回显示此对象值的用户友好字符串。 |

## 字段

| 姓名 | 描述 |
| --- | --- |
| static readonly [Auto](../../aspose.words.tables/preferredwidth/auto/) | 返回一个表示“未指定首选宽度”值的实例。 |

### 评论

首选宽度可以指定为百分比、点数或特殊的“无/自动”值。

这个类的实例是不可变的。

### 例子

演示如何将表格设置为自动适应页面宽度的 50%。

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

显示如何为表格单元格设置首选宽度。

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

// 没有指定首选宽度的单元格将占用剩余的可用空间。
builder.CellFormat.PreferredWidth = PreferredWidth.Auto;

// “PreferredWidth”属性的每个配置都会创建一个新对象。
Assert.AreNotEqual(table.FirstRow.Cells[1].CellFormat.PreferredWidth.GetHashCode(),
    builder.CellFormat.PreferredWidth.GetHashCode());

builder.CellFormat.Shading.BackgroundPatternColor = Color.LightGreen;
builder.Writeln("Automatically sized cell.");

doc.Save(ArtifactsDir + "DocumentBuilder.InsertCellsWithPreferredWidths.docx");
```

### 也可以看看

* 命名空间 [Aspose.Words.Tables](../../aspose.words.tables/)
* 部件 [Aspose.Words](../../)


