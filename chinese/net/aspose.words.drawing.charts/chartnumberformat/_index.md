---
title: ChartNumberFormat Class
linktitle: ChartNumberFormat
articleTitle: ChartNumberFormat
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Drawing.Charts.ChartNumberFormat 类，实现图表中的高级数字格式。提升文档的视觉吸引力！
type: docs
weight: 1060
url: /zh/net/aspose.words.drawing.charts/chartnumberformat/
---
## ChartNumberFormat class

表示父元素的数字格式。

要了解更多信息，请访问[使用图表](https://docs.aspose.com/words/net/working-with-charts/)文档文章。

```csharp
public class ChartNumberFormat
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [FormatCode](../../aspose.words.drawing.charts/chartnumberformat/formatcode/) { get; set; } | 获取或设置应用于数据标签的格式代码。 |
| [IsLinkedToSource](../../aspose.words.drawing.charts/chartnumberformat/islinkedtosource/) { get; set; } | 指定格式代码是否链接到源单元格。 默认值为 true。 |

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

* 命名空间 [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* 部件 [Aspose.Words](../../)
