---
title: Chart.SeriesGroups
linktitle: SeriesGroups
articleTitle: SeriesGroups
second_title: Aspose.Words for .NET
description: 探索图表 SeriesGroups 属性，轻松访问丰富的系列组集合，增强您的数据可视化体验。
type: docs
weight: 90
url: /zh/net/aspose.words.drawing.charts/chart/seriesgroups/
---
## Chart.SeriesGroups property

提供对此图表的系列组集合的访问。

```csharp
public ChartSeriesGroupCollection SeriesGroups { get; }
```

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

* class [ChartSeriesGroupCollection](../../chartseriesgroupcollection/)
* class [Chart](../)
* 命名空间 [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* 部件 [Aspose.Words](../../../)
