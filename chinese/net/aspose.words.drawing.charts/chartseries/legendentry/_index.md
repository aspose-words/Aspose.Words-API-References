---
title: ChartSeries.LegendEntry
linktitle: LegendEntry
articleTitle: LegendEntry
second_title: Aspose.Words for .NET
description: 探索 ChartSeries LegendEntry 属性，轻松访问和自定义图表的图例条目，增强数据可视化。
type: docs
weight: 90
url: /zh/net/aspose.words.drawing.charts/chartseries/legendentry/
---
## ChartSeries.LegendEntry property

获取此图表系列的图例条目。

```csharp
public ChartLegendEntry LegendEntry { get; }
```

## 例子

展示如何使用图例字体。

```csharp
Document doc = new Document(MyDir + "Reporting engine template - Chart series.docx");
Chart chart = ((Shape)doc.GetChild(NodeType.Shape, 0, true)).Chart;

ChartLegend chartLegend = chart.Legend;
// 设置所有图例条目的默认字体大小。
chartLegend.Font.Size = 14;
// 更改特定图例条目的字体。
chartLegend.LegendEntries[1].Font.Italic = true;
chartLegend.LegendEntries[1].Font.Size = 12;
// 获取图表系列的图例条目。
ChartLegendEntry legendEntry = chart.Series[0].LegendEntry;

doc.Save(ArtifactsDir + "Charts.LegendFont.docx");
```

### 也可以看看

* class [ChartLegendEntry](../../chartlegendentry/)
* class [ChartSeries](../)
* 命名空间 [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* 部件 [Aspose.Words](../../../)
