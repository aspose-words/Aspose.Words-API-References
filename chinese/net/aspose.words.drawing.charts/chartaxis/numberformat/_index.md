---
title: ChartAxis.NumberFormat
linktitle: NumberFormat
articleTitle: NumberFormat
second_title: Aspose.Words for .NET
description: 探索 ChartAxis NumberFormat 属性，使用 ChartNumberFormat 对象轻松自定义图表的数字格式，从而增强数据可视化。
type: docs
weight: 200
url: /zh/net/aspose.words.drawing.charts/chartaxis/numberformat/
---
## ChartAxis.NumberFormat property

返回[`ChartNumberFormat`](../../chartnumberformat/)允许定义轴的数字格式的对象。

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

### 也可以看看

* class [ChartNumberFormat](../../chartnumberformat/)
* class [ChartAxis](../)
* 命名空间 [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* 部件 [Aspose.Words](../../../)
