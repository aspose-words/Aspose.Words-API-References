---
title: ChartNumberFormat.FormatCode
linktitle: FormatCode
articleTitle: FormatCode
second_title: Aspose.Words for .NET
description: 了解如何使用 ChartNumberFormat FormatCode 属性自定义数据标签格式，以获得更清晰的见解和增强的数据呈现。
type: docs
weight: 10
url: /zh/net/aspose.words.drawing.charts/chartnumberformat/formatcode/
---
## ChartNumberFormat.FormatCode property

获取或设置应用于数据标签的格式代码。

```csharp
public string FormatCode { get; set; }
```

## 评论

数字格式用于改变值在数据标签中的显示方式，并且可以以一些非常有创意的方式使用。 数字格式的示例：

数字 - “#,##0.00”

货币 - "\"$\"#,##0.00"

时间 - “[$-x-systime]h:mm:ss AM/PM”

日期 - “d/mm/yyyy”

百分比 - “0.00%”

分数 - ”＃ ？/？”

科学的——“0.00E+00”

文本 - ”@”

会计 - "_-\"$\"* #,##0.00_-;-\"$\"* #,##0.00_-;_-\"$\"* \"-\"??_-;_-@_-"

自定义颜色 - “[红色]-#,##0.0”

## 例子

显示如何设置图表值的格式。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 500, 300);
Chart chart = shape.Chart;

// 清除图表的演示数据系列以从干净的图表开始。
chart.Series.Clear();

// 向图表中添加自定义系列，其中包含 X 轴的类别，
 // 以及 Y 轴的相应较大数值。
chart.Series.Add("Aspose Test Series",
    new[] { "Word", "PDF", "Excel", "GoogleDocs", "Note" },
    new double[] { 1900000, 850000, 2100000, 600000, 1500000 });

 // 设置 Y 轴刻度标签的数字格式，不使用逗号对数字进行分组。
chart.AxisY.NumberFormat.FormatCode = "#,##0";

// 此标志可以覆盖上述值并从源单元格绘制数字格式。
Assert.False(chart.AxisY.NumberFormat.IsLinkedToSource);

doc.Save(ArtifactsDir + "Charts.SetNumberFormatToChartAxis.docx");
```

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

* class [ChartNumberFormat](../)
* 命名空间 [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* 部件 [Aspose.Words](../../../)
