---
title: ChartDataLabel.ShowBubbleSize
linktitle: ShowBubbleSize
articleTitle: ShowBubbleSize
second_title: 用于 .NET 的 Aspose.Words
description: ChartDataLabel ShowBubbleSize 财产. 允许指定是否为图表上的数据标签显示气泡大小 仅适用于气泡图 默认值为错误的 在 C#.
type: docs
weight: 80
url: /zh/net/aspose.words.drawing.charts/chartdatalabel/showbubblesize/
---
## ChartDataLabel.ShowBubbleSize property

允许指定是否为图表上的数据标签显示气泡大小。 仅适用于气泡图。 默认值为`错误的`.

```csharp
public bool ShowBubbleSize { get; set; }
```

## 例子

展示如何将 3D 效果与气泡图结合使用。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Bubble3D, 500, 350);
Chart chart = shape.Chart;

Assert.AreEqual(1, chart.Series.Count);
Assert.AreEqual("Y-Values", chart.Series[0].Name);
Assert.True(chart.Series[0].Bubble3D);

// 将数据标签应用于显示其直径的每个气泡。
for (int i = 0; i < 3; i++)
{
    chart.Series[0].HasDataLabels = true;
    chart.Series[0].DataLabels[i].ShowBubbleSize = true;
    chart.Series[0].DataLabels[i].Font.Size = 12;
}

doc.Save(ArtifactsDir + "Charts.Bubble3D.docx");
```

### 也可以看看

* class [ChartDataLabel](../)
* 命名空间 [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* 部件 [Aspose.Words](../../../)
