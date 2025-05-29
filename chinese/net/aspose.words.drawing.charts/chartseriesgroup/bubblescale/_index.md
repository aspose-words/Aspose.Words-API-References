---
title: ChartSeriesGroup.BubbleScale
linktitle: BubbleScale
articleTitle: BubbleScale
second_title: Aspose.Words for .NET
description: 探索 ChartSeriesGroup BubbleScale 属性以自定义图表中的气泡大小，增强数据可视化和用户参与度。
type: docs
weight: 40
url: /zh/net/aspose.words.drawing.charts/chartseriesgroup/bubblescale/
---
## ChartSeriesGroup.BubbleScale property

获取或设置气泡的大小（以其默认大小的百分比表示）。

```csharp
public int BubbleScale { get; set; }
```

## 评论

仅适用于Bubbleand Bubble3D类型。

可接受值的范围是 0 到 300（含）。默认值为 100。

## 例子

展示如何设置气泡的大小。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 插入气泡 3D 图表。
Shape shape = builder.InsertChart(ChartType.Bubble3D, 450, 250);
ChartSeriesGroup seriesGroup = shape.Chart.SeriesGroups[0];

// 将气泡比例设置为 200%。
seriesGroup.BubbleScale = 200;

doc.Save(ArtifactsDir + "Charts.BubbleScale.docx");
```

### 也可以看看

* class [ChartSeriesGroup](../)
* 命名空间 [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* 部件 [Aspose.Words](../../../)
