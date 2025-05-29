---
title: ChartSeriesGroup.GapWidth
linktitle: GapWidth
articleTitle: GapWidth
second_title: Aspose.Words for .NET
description: 探索 ChartSeriesGroup GapWidth 属性，轻松调整图表元素之间的间隙百分比，以增强数据可视化。
type: docs
weight: 70
url: /zh/net/aspose.words.drawing.charts/chartseriesgroup/gapwidth/
---
## ChartSeriesGroup.GapWidth property

获取或设置图表元素之间的间隙宽度百分比。

```csharp
public int GapWidth { get; set; }
```

## 评论

仅适用于条形图、柱形图、饼图、饼图、直方图、箱线图、瀑布图和漏斗类型的系列组。

可接受值的范围是 0 到 500（含）。对于基于条形/柱形的系列组， 属性表示条形簇之间的间距占其宽度的百分比。对于饼图中的饼图和 条图中的饼图，此值表示图表主要部分和次要部分之间的间距。

## 例子

展示如何配置间隙宽度和重叠。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 450, 250);
ChartSeriesGroup seriesGroup = shape.Chart.SeriesGroups[0];

// 设置列间隙宽度和重叠。
seriesGroup.GapWidth = 450;
seriesGroup.Overlap = -75;

doc.Save(ArtifactsDir + "Charts.ConfigureGapOverlap.docx");
```

### 也可以看看

* class [ChartSeriesGroup](../)
* 命名空间 [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* 部件 [Aspose.Words](../../../)
