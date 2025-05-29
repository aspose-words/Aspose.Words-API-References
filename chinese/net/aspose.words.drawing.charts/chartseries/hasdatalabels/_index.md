---
title: ChartSeries.HasDataLabels
linktitle: HasDataLabels
articleTitle: HasDataLabels
second_title: Aspose.Words for .NET
description: 探索 ChartSeries HasDataLabels 属性，轻松管理系列的数据标签可见性，增强数据可视化体验。
type: docs
weight: 70
url: /zh/net/aspose.words.drawing.charts/chartseries/hasdatalabels/
---
## ChartSeries.HasDataLabels property

获取或设置一个标志，指示是否显示系列的数据标签。

```csharp
public bool HasDataLabels { get; set; }
```

## 例子

展示如何启用和配置图表系列的数据标签。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 添加折线图，然后清除其演示数据系列以从干净的图表开始，
// 然后设置标题。
Shape shape = builder.InsertChart(ChartType.Line, 500, 300);
Chart chart = shape.Chart;
chart.Series.Clear();
chart.Title.Text = "Monthly sales report";

// 插入以月份作为 X 轴类别的自定义图表系列，
// 以及 Y 轴的相应小数。
ChartSeries series = chart.Series.Add("Revenue",
    new[] { "January", "February", "March" },
    new[] { 25.611d, 21.439d, 33.750d });

// 启用数据标签，然后对数据标签中显示的值应用自定义数字格式。
// 此格式将显示的十进制值视为百万美元。
series.HasDataLabels = true;
ChartDataLabelCollection dataLabels = series.DataLabels;
dataLabels.ShowValue = true;
dataLabels.NumberFormat.FormatCode = "\"US$\" #,##0.000\"M\"";
dataLabels.Font.Size = 12;

doc.Save(ArtifactsDir + "Charts.DataLabelNumberFormat.docx");
```

### 也可以看看

* class [ChartSeries](../)
* 命名空间 [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* 部件 [Aspose.Words](../../../)
