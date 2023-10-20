---
title: ChartAxis.NumberFormat
linktitle: NumberFormat
articleTitle: NumberFormat
second_title: 用于 .NET 的 Aspose.Words
description: ChartAxis NumberFormat 财产. 返回一个ChartNumberFormat允许为轴定义数字格式的对象 在 C#.
type: docs
weight: 190
url: /zh/net/aspose.words.drawing.charts/chartaxis/numberformat/
---
## ChartAxis.NumberFormat property

返回一个[`ChartNumberFormat`](../../chartnumberformat/)允许为轴定义数字格式的对象。

```csharp
public ChartNumberFormat NumberFormat { get; }
```

## 例子

显示如何设置图表值的格式。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 500, 300);
Chart chart = shape.Chart;

// 清除图表的演示数据系列以从干净的图表开始。
chart.Series.Clear();

// 将自定义系列添加到图表中，X 轴为类别，
 // 以及 Y 轴的相应大数值。
chart.Series.Add("Aspose Test Series",
    new [] { "Word", "PDF", "Excel", "GoogleDocs", "Note" },
    new double[] { 1900000, 850000, 2100000, 600000, 1500000 });

 // 将 Y 轴刻度标签的数字格式设置为不使用逗号分组数字。
chart.AxisY.NumberFormat.FormatCode = "#,##0";

// 这个标志可以覆盖上面的值并从源单元格中绘制数字格式。
Assert.False(chart.AxisY.NumberFormat.IsLinkedToSource);

doc.Save(ArtifactsDir + "Charts.SetNumberFormatToChartAxis.docx");
```

### 也可以看看

* class [ChartNumberFormat](../../chartnumberformat/)
* class [ChartAxis](../)
* 命名空间 [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* 部件 [Aspose.Words](../../../)
