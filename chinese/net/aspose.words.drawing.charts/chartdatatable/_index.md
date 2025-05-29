---
title: ChartDataTable Class
linktitle: ChartDataTable
articleTitle: ChartDataTable
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Drawing.Charts.ChartDataTable 类，轻松自定义图表数据表并使用强大的功能增强数据可视化。
type: docs
weight: 990
url: /zh/net/aspose.words.drawing.charts/chartdatatable/
---
## ChartDataTable class

允许指定图表数据表的属性。

```csharp
public class ChartDataTable
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [Font](../../aspose.words.drawing.charts/chartdatatable/font/) { get; } | 提供对数据表字体格式的访问。 |
| [Format](../../aspose.words.drawing.charts/chartdatatable/format/) { get; } | 提供对数据表的文本背景填充和边框格式的访问。 |
| [HasHorizontalBorder](../../aspose.words.drawing.charts/chartdatatable/hashorizontalborder/) { get; set; } | 获取或设置是否显示数据表水平边框的标志。 默认值为`真的`. |
| [HasLegendKeys](../../aspose.words.drawing.charts/chartdatatable/haslegendkeys/) { get; set; } | 获取或设置一个标志，指示图例键是否显示在数据表中。 默认值为`真的`. |
| [HasOutlineBorder](../../aspose.words.drawing.charts/chartdatatable/hasoutlineborder/) { get; set; } | 获取或设置一个标志，指示是否显示轮廓边框，即系列和类别名称周围的边框。 默认值为`真的`. |
| [HasVerticalBorder](../../aspose.words.drawing.charts/chartdatatable/hasverticalborder/) { get; set; } | 获取或设置是否显示数据表垂直边框的标志。 默认值为`真的`. |
| [Show](../../aspose.words.drawing.charts/chartdatatable/show/) { get; set; } | 获取或设置一个标志，指示是否显示图表的数据表。 默认值为`错误的`. |

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

* 命名空间 [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* 部件 [Aspose.Words](../../)
