---
title: ChartXValue.FromString
linktitle: FromString
articleTitle: FromString
second_title: 用于 .NET 的 Aspose.Words
description: ChartXValue FromString 方法. 创建一个ChartXValue的实例String类型 在 C#.
type: docs
weight: 40
url: /zh/net/aspose.words.drawing.charts/chartxvalue/fromstring/
---
## ChartXValue.FromString method

创建一个[`ChartXValue`](../)的实例String类型.

```csharp
public static ChartXValue FromString(string value)
```

## 例子

展示如何添加/删除图表数据值。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder();

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);
Chart chart = shape.Chart;
ChartSeries department1Series = chart.Series[0];
ChartSeries department2Series = chart.Series[1];

// 删除两个系列中的第一个值。
department1Series.Remove(0);
department2Series.Remove(0);

// 向两个系列添加新值。
ChartXValue newXCategory = ChartXValue.FromString("Q1, 2023");
department1Series.Add(newXCategory, ChartYValue.FromDouble(10.3));
department2Series.Add(newXCategory, ChartYValue.FromDouble(5.7));

doc.Save(ArtifactsDir + "Charts.ChartDataValues.docx");
```

### 也可以看看

* class [ChartXValue](../)
* 命名空间 [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* 部件 [Aspose.Words](../../../)
