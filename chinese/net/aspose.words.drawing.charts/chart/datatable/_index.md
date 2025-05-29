---
title: Chart.DataTable
linktitle: DataTable
articleTitle: DataTable
second_title: Aspose.Words for .NET
description: 轻松访问和自定义图表的 DataTable 属性。使用“Show”属性增强数据可视化，获得更清晰的洞察。
type: docs
weight: 50
url: /zh/net/aspose.words.drawing.charts/chart/datatable/
---
## Chart.DataTable property

提供对此图表数据表属性的访问。 可以使用[`Show`](../../chartdatatable/show/)属性.

```csharp
public ChartDataTable DataTable { get; }
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

* class [ChartDataTable](../../chartdatatable/)
* class [Chart](../)
* 命名空间 [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* 部件 [Aspose.Words](../../../)
