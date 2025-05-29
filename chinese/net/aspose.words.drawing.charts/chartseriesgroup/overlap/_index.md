---
title: ChartSeriesGroup.Overlap
linktitle: Overlap
articleTitle: Overlap
second_title: Aspose.Words for .NET
description: 探索 ChartSeriesGroup Overlap 属性，轻松调整系列条或列的重叠百分比，以增强数据可视化。
type: docs
weight: 80
url: /zh/net/aspose.words.drawing.charts/chartseriesgroup/overlap/
---
## ChartSeriesGroup.Overlap property

获取或设置系列条形或柱形重叠的百分比。

```csharp
public int Overlap { get; set; }
```

## 评论

适用于所有条形和柱形类型的系列组。

可接受值的范围是 -100 到 100（含）。值为 0 表示条/列之间没有 空间。如果值为 -100，则条/列之间的距离等于其宽度。值为 100 表示条/列完全重叠。

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
