---
title: ChartDataTable.HasOutlineBorder
linktitle: HasOutlineBorder
articleTitle: HasOutlineBorder
second_title: Aspose.Words for .NET
description: 发现 ChartDataTable HasOutlineBorder 属性，控制系列和类别名称周围的轮廓边框的显示，以增强数据清晰度。
type: docs
weight: 50
url: /zh/net/aspose.words.drawing.charts/chartdatatable/hasoutlineborder/
---
## ChartDataTable.HasOutlineBorder property

获取或设置一个标志，指示是否显示轮廓边框，即系列和类别名称周围的边框。 默认值为`真的`.

```csharp
public bool HasOutlineBorder { get; set; }
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
