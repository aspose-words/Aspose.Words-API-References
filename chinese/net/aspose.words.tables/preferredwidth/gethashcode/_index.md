---
title: PreferredWidth.GetHashCode
linktitle: GetHashCode
articleTitle: GetHashCode
second_title: 用于 .NET 的 Aspose.Words
description: PreferredWidth GetHashCode 方法. 用作此类型的哈希函数 在 C#.
type: docs
weight: 70
url: /zh/net/aspose.words.tables/preferredwidth/gethashcode/
---
## PreferredWidth.GetHashCode method

用作此类型的哈希函数。

```csharp
public override int GetHashCode()
```

## 例子

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
* 命名空间 [Aspose.Words.Tables](../../../aspose.words.tables/)
* 部件 [Aspose.Words](../../../)
