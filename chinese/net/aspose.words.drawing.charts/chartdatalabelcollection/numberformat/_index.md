---
title: ChartDataLabelCollection.NumberFormat
linktitle: NumberFormat
articleTitle: NumberFormat
second_title: Aspose.Words for .NET
description: 探索 ChartDataLabelCollection NumberFormat 属性，轻松自定义整个系列的数据标签格式，增强清晰度和演示效果。
type: docs
weight: 50
url: /zh/net/aspose.words.drawing.charts/chartdatalabelcollection/numberformat/
---
## ChartDataLabelCollection.NumberFormat property

获取[`ChartNumberFormat`](../../chartnumberformat/)允许为整个系列的数据标签设置数字格式的实例。

```csharp
public ChartNumberFormat NumberFormat { get; }
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

* class [ChartNumberFormat](../../chartnumberformat/)
* class [ChartDataLabelCollection](../)
* 命名空间 [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* 部件 [Aspose.Words](../../../)
