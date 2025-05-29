---
title: ChartDataTable.HasHorizontalBorder
linktitle: HasHorizontalBorder
articleTitle: HasHorizontalBorder
second_title: Aspose.Words for .NET
description: 探索 ChartDataTable HasHorizontalBorder 属性，轻松自定义数据表的外观。控制水平边框，提升视觉清晰度！
type: docs
weight: 30
url: /zh/net/aspose.words.drawing.charts/chartdatatable/hashorizontalborder/
---
## ChartDataTable.HasHorizontalBorder property

获取或设置是否显示数据表水平边框的标志。 默认值为`真的`.

```csharp
public bool HasHorizontalBorder { get; set; }
```

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
