---
title: ChartSeries.Remove
linktitle: Remove
articleTitle: Remove
second_title: Aspose.Words for .NET
description: 使用 ChartSeries Remove 方法，轻松移除图表系列中的 X 值、Y 值和气泡大小。立即简化您的数据可视化！
type: docs
weight: 210
url: /zh/net/aspose.words.drawing.charts/chartseries/remove/
---
## ChartSeries.Remove method

从指定索引处的图表系列中删除 X 值、Y 值和气泡大小（如果支持）。 相应的数据点和数据标签也将被删除。

```csharp
public void Remove(int index)
```

## 例子

显示如何添加/删除图表数据值。

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

* class [ChartSeries](../)
* 命名空间 [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* 部件 [Aspose.Words](../../../)
