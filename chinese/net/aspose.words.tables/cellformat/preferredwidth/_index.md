---
title: CellFormat.PreferredWidth
linktitle: PreferredWidth
articleTitle: PreferredWidth
second_title: Aspose.Words for .NET
description: 探索 CellFormat PreferredWidth 属性，轻松自定义单元格宽度，实现电子表格的最佳布局和设计。提升您的数据呈现效果！
type: docs
weight: 80
url: /zh/net/aspose.words.tables/cellformat/preferredwidth/
---
## CellFormat.PreferredWidth property

返回或设置单元格的首选宽度。

```csharp
public PreferredWidth PreferredWidth { get; set; }
```

## 评论

首选宽度（以及表格的“自动调整”选项）决定了表格布局算法如何计算单元格的实际宽度。表格布局可以由 Aspose.Words 在保存文档时执行，也可以由 Microsoft Word 在显示文档时执行。

首选宽度可以用磅或百分比来指定。首选宽度 也可以指定为“auto”，即不指定首选宽度。

默认值为[`Auto`](../../preferredwidth/auto/)。

## 例子

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

* class [PreferredWidth](../../preferredwidth/)
* class [CellFormat](../)
* 命名空间 [Aspose.Words.Tables](../../../aspose.words.tables/)
* 部件 [Aspose.Words](../../../)
