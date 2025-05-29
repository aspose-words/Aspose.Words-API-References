---
title: ChartAxisTitle.Format
linktitle: Format
articleTitle: Format
second_title: Aspose.Words for .NET
description: 发现 ChartAxisTitle 格式属性，轻松自定义轴标题填充和线条样式，增强数据可视化。
type: docs
weight: 20
url: /zh/net/aspose.words.drawing.charts/chartaxistitle/format/
---
## ChartAxisTitle.Format property

提供对轴标题的填充和线条格式的访问。

```csharp
public ChartFormat Format { get; }
```

## 例子

展示如何使用图表格式。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);
Chart chart = shape.Chart;

// 删除默认生成的系列。
ChartSeriesCollection series = chart.Series;
series.Clear();

string[] categories = new string[] { "Category 1", "Category 2" };
series.Add("Series 1", categories, new double[] { 1, 2 });
series.Add("Series 2", categories, new double[] { 3, 4 });

// 格式化图表背景。
chart.Format.Fill.Solid(Color.DarkSlateGray);

// 隐藏轴刻度标签。
chart.AxisX.TickLabels.Position = AxisTickLabelPosition.None;
chart.AxisY.TickLabels.Position = AxisTickLabelPosition.None;

// 格式化图表标题。
chart.Title.Format.Fill.Solid(Color.LightGoldenrodYellow);

// 格式化轴标题。
chart.AxisX.Title.Show = true;
chart.AxisX.Title.Format.Fill.Solid(Color.LightGoldenrodYellow);

// 格式化图例。
chart.Legend.Format.Fill.Solid(Color.LightGoldenrodYellow);

doc.Save(ArtifactsDir + "Charts.ChartFormat.docx");
```

### 也可以看看

* class [ChartFormat](../../chartformat/)
* class [ChartAxisTitle](../)
* 命名空间 [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* 部件 [Aspose.Words](../../../)
