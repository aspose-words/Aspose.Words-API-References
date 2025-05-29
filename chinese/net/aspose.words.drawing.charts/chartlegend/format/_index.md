---
title: ChartLegend.Format
linktitle: Format
articleTitle: Format
second_title: Aspose.Words for .NET
description: 发现 ChartLegend Format 属性，轻松自定义图例填充和线条样式，增强您的数据可视化体验。
type: docs
weight: 20
url: /zh/net/aspose.words.drawing.charts/chartlegend/format/
---
## ChartLegend.Format property

提供对图例的填充和线条格式的访问。

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
* class [ChartLegend](../)
* 命名空间 [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* 部件 [Aspose.Words](../../../)
