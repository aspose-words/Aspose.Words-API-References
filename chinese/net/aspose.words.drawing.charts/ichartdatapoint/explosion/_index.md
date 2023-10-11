---
title: IChartDataPoint.Explosion
second_title: Aspose.Words for .NET API 参考
description: IChartDataPoint 财产. 指定数据点应从饼图中心移动的量 可以为负数负数表示未设置属性且不应应用爆炸 仅适用于饼图
type: docs
weight: 20
url: /zh/net/aspose.words.drawing.charts/ichartdatapoint/explosion/
---
## IChartDataPoint.Explosion property

指定数据点应从饼图中心移动的量。 可以为负数，负数表示未设置属性且不应应用爆炸。 仅适用于饼图。

```csharp
public int Explosion { get; set; }
```

### 例子

演示如何将饼图的切片移离中心。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Pie, 500, 350);
Chart chart = shape.Chart;

Assert.AreEqual(1, chart.Series.Count);
Assert.AreEqual("Sales", chart.Series[0].Name);

// 饼图的“切片”可以通过相应数据点的爆炸属性从中心移开一段距离。
// 将一个数据点添加到饼图的第一部分，并将其移离中心 10 点。
// 如果数据点不存在，Aspose.Words 会自动创建数据点。
ChartDataPoint dataPoint = chart.Series[0].DataPoints[0];
dataPoint.Explosion = 10;

// 将第二部分移动更大的距离。
dataPoint = chart.Series[0].DataPoints[1];
dataPoint.Explosion = 40;

doc.Save(ArtifactsDir + "Charts.PieChartExplosion.docx");
```

### 也可以看看

* interface [IChartDataPoint](../)
* 命名空间 [Aspose.Words.Drawing.Charts](../../ichartdatapoint/)
* 部件 [Aspose.Words](../../../)


