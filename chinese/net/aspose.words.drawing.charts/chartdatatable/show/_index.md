---
title: ChartDataTable.Show
linktitle: Show
articleTitle: Show
second_title: Aspose.Words for .NET
description: 使用 ChartDataTable 的 Show 属性控制图表的可见性。轻松切换数据表显示，增强数据洞察。默认值为 false。
type: docs
weight: 70
url: /zh/net/aspose.words.drawing.charts/chartdatatable/show/
---
## ChartDataTable.Show property

获取或设置一个标志，指示是否显示图表的数据表。 默认值为`错误的`.

```csharp
public bool Show { get; set; }
```

## 评论

以下图表类型不支持数据表：散点图、饼图、圆环图、曲面图、雷达图、树形图、旭日图、直方图、排列图、箱线图、瀑布图、漏斗图、包含一系列这些类型的组合图。显示这些图表类型的数据表会引发InvalidOperationException 异常.

## 例子

展示如何使用图表系列数据显示数据表。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);
Chart chart = shape.Chart;

ChartSeriesCollection series = chart.Series;
series.Clear();
double[] xValues = new double[] { 2020, 2021, 2022, 2023 };
series.Add("Series1", xValues, new double[] { 5, 11, 2, 7 });
series.Add("Series2", xValues, new double[] { 6, 5.5, 7, 7.8 });
series.Add("Series3", xValues, new double[] { 10, 8, 7, 9 });

ChartDataTable dataTable = chart.DataTable;
dataTable.Show = true;

dataTable.HasLegendKeys = false;
dataTable.HasHorizontalBorder = false;
dataTable.HasVerticalBorder = false;
dataTable.HasOutlineBorder = false;

dataTable.Font.Italic = true;
dataTable.Format.Stroke.Weight = 1;
dataTable.Format.Stroke.DashStyle = DashStyle.ShortDot;
dataTable.Format.Stroke.Color = Color.DarkBlue;

doc.Save(ArtifactsDir + "Charts.DataTable.docx");
```

### 也可以看看

* class [ChartDataTable](../)
* 命名空间 [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* 部件 [Aspose.Words](../../../)
