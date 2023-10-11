---
title: ChartNumberFormat.FormatCode
second_title: Aspose.Words for .NET API 参考
description: ChartNumberFormat 财产. 获取或设置应用于数据标签的格式代码
type: docs
weight: 10
url: /zh/net/aspose.words.drawing.charts/chartnumberformat/formatcode/
---
## ChartNumberFormat.FormatCode property

获取或设置应用于数据标签的格式代码。

```csharp
public string FormatCode { get; set; }
```

### 评论

数字格式用于更改值在数据标签中的显示方式，并且可以以一些非常有创意的方式使用。 数字格式的示例：

数字 - “#,##0.00”

货币 - "\"$\"#,##0.00"

时间 - “[$-x-systime]h:mm:ss AM/PM”

日期 - “日/月/年”

百分比 - “0.00%”

分数 - ”＃ ？/？”

科学-“0.00E+00”

文本 - ”@”

会计 - "_-\"$\"* #,##0.00_-;-\"$\"* #,##0.00_-;_-\"$\"* \"-\"??_ -;_-@_-”

自定义颜色 - “[红色]-#,##0.0”

### 例子

展示如何设置图表值的格式。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 500, 300);
Chart chart = shape.Chart;

// 清除图表的演示数据系列以从干净的图表开始。
chart.Series.Clear();

// 将自定义系列添加到图表中，其中 X 轴为类别，
 // 和 Y 轴各自较大的数值。
chart.Series.Add("Aspose Test Series",
    new [] { "Word", "PDF", "Excel", "GoogleDocs", "Note" },
    new double[] { 1900000, 850000, 2100000, 600000, 1500000 });

 // 将 Y 轴刻度标签的数字格式设置为不使用逗号对数字进行分组。
chart.AxisY.NumberFormat.FormatCode = "#,##0";

// 该标志可以覆盖上面的值并从源单元格中绘制数字格式。
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

// 插入自定义图表系列，以月份作为 X 轴的类别，
// 以及 Y 轴的相应小数量。
ChartSeries series = chart.Series.Add("Revenue", 
    new[] { "January", "February", "March" }, 
    new[] { 25.611d, 21.439d, 33.750d });

// 启用数据标签，然后为数据标签中显示的值应用自定义数字格式。
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
* 命名空间 [Aspose.Words.Drawing.Charts](../../chartnumberformat/)
* 部件 [Aspose.Words](../../../)


