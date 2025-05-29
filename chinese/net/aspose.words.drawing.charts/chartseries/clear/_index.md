---
title: ChartSeries.Clear
linktitle: Clear
articleTitle: Clear
second_title: Aspose.Words for .NET
description: 使用 ChartSeries Clear 方法优化您的图表！轻松删除数据值并重置格式，打造更简洁、更专业的外观。
type: docs
weight: 170
url: /zh/net/aspose.words.drawing.charts/chartseries/clear/
---
## ChartSeries.Clear method

从图表系列中删除所有数据值。所有单个数据点和数据标签的格式均被清除。

```csharp
public void Clear()
```

## 例子

展示如何用数据填充图表系列。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);
Chart chart = shape.Chart;
ChartSeries series1 = chart.Series[0];

// 清除第一个系列的 X 和 Y 值。
series1.ClearValues();

// 用数据填充系列。
series1.Add(ChartXValue.FromDouble(3), ChartYValue.FromDouble(10), 10);
series1.Add(ChartXValue.FromDouble(5), ChartYValue.FromDouble(5));
series1.Add(ChartXValue.FromDouble(7), ChartYValue.FromDouble(11));
series1.Add(ChartXValue.FromDouble(9));

ChartSeries series2 = chart.Series[1];
// 清除第二个系列的 X 和 Y 值。
series2.Clear();

// 用数据填充系列。
series2.Add(ChartXValue.FromDouble(2), ChartYValue.FromDouble(4));
series2.Add(ChartXValue.FromDouble(4), ChartYValue.FromDouble(7));
series2.Add(ChartXValue.FromDouble(6), ChartYValue.FromDouble(14));
series2.Add(ChartXValue.FromDouble(8), ChartYValue.FromDouble(7));

doc.Save(ArtifactsDir + "Charts.PopulateChartWithData.docx");
```

### 也可以看看

* class [ChartSeries](../)
* 命名空间 [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* 部件 [Aspose.Words](../../../)
