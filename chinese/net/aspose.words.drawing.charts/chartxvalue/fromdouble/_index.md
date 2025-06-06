---
title: ChartXValue.FromDouble
linktitle: FromDouble
articleTitle: FromDouble
second_title: Aspose.Words for .NET
description: 探索 ChartXValue FromDouble 方法，轻松创建 Double 类型的 ChartXValue 实例，增强您的数据可视化能力。
type: docs
weight: 20
url: /zh/net/aspose.words.drawing.charts/chartxvalue/fromdouble/
---
## ChartXValue.FromDouble method

创建一个[`ChartXValue`](../)的实例Double类型.

```csharp
public static ChartXValue FromDouble(double value)
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

* class [ChartXValue](../)
* 命名空间 [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* 部件 [Aspose.Words](../../../)
