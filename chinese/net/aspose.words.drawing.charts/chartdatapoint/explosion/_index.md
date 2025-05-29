---
title: ChartDataPoint.Explosion
linktitle: Explosion
articleTitle: Explosion
second_title: Aspose.Words for .NET
description: 探索 ChartDataPoint Explosion 属性，调整饼图数据点。从中心控制移动，打造更具影响力的可视化效果。立即提升您的图表！
type: docs
weight: 20
url: /zh/net/aspose.words.drawing.charts/chartdatapoint/explosion/
---
## ChartDataPoint.Explosion property

指定数据点应从饼图中心移动的量。 可以为负数，负数表示未设置属性，不应应用爆炸。 仅适用于饼图。

```csharp
public int Explosion { get; set; }
```

## 例子

展示如何将饼图的各个部分移离中心。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Pie, 500, 350);
Chart chart = shape.Chart;

Assert.AreEqual(1, chart.Series.Count);
Assert.AreEqual("Sales", chart.Series[0].Name);

// 可以通过相应数据点的 Explosion 属性将饼图的“切片”从中心移开一定距离。
// 在饼图的第一部分添加一个数据点，并将其从中心移动 10 个点。
// 如果数据点不存在，Aspose.Words 会自动创建数据点。
ChartDataPoint dataPoint = chart.Series[0].DataPoints[0];
dataPoint.Explosion = 10;

// 将第二部分移动更大的距离。
dataPoint = chart.Series[0].DataPoints[1];
dataPoint.Explosion = 40;

doc.Save(ArtifactsDir + "Charts.PieChartExplosion.docx");
```

### 也可以看看

* class [ChartDataPoint](../)
* 命名空间 [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* 部件 [Aspose.Words](../../../)
