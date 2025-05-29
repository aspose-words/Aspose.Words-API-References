---
title: IChartDataPoint.Bubble3D
linktitle: Bubble3D
articleTitle: Bubble3D
second_title: Aspose.Words for .NET
description: 探索 IChartDataPoint Bubble3D 属性，以令人惊叹的 3D 效果增强您的气泡图，实现更具吸引力的数据可视化。
type: docs
weight: 10
url: /zh/net/aspose.words.drawing.charts/ichartdatapoint/bubble3d/
---
## IChartDataPoint.Bubble3D property

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

* interface [IChartDataPoint](../)
* 命名空间 [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* 部件 [Aspose.Words](../../../)
