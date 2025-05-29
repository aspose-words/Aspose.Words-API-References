---
title: ChartSeries.Bubble3D
linktitle: Bubble3D
articleTitle: Bubble3D
second_title: Aspose.Words for .NET
description: 使用 ChartSeries Bubble3D 增强你的气泡图！为气泡图添加炫目的 3D 效果，打造引人注目的视觉效果。
type: docs
weight: 10
url: /zh/net/aspose.words.drawing.charts/chartseries/bubble3d/
---
## ChartSeries.Bubble3D property

指定气泡图中的气泡是否应用三维效果。

```csharp
public bool Bubble3D { get; set; }
```

## 例子

展示如何在气泡图中使用 3D 效果。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Bubble3D, 500, 350);
Chart chart = shape.Chart;

Assert.AreEqual(1, chart.Series.Count);
Assert.AreEqual("Y-Values", chart.Series[0].Name);
Assert.True(chart.Series[0].Bubble3D);

// 为每个显示其直径的气泡应用数据标签。
for (int i = 0; i < 3; i++)
{
    chart.Series[0].HasDataLabels = true;
    chart.Series[0].DataLabels[i].ShowBubbleSize = true;
    chart.Series[0].DataLabels[i].Font.Size = 12;
}

doc.Save(ArtifactsDir + "Charts.Bubble3D.docx");
```

### 也可以看看

* class [ChartSeries](../)
* 命名空间 [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* 部件 [Aspose.Words](../../../)
