---
title: ChartSeries.SeriesType
linktitle: SeriesType
articleTitle: SeriesType
second_title: Aspose.Words for .NET
description: 探索 ChartSeries 的 SeriesType 属性，轻松识别图表系列类型，增强数据可视化效果。立即解锁强大的洞察！
type: docs
weight: 120
url: /zh/net/aspose.words.drawing.charts/chartseries/seriestype/
---
## ChartSeries.SeriesType property

获取此图表系列的类型。

```csharp
public ChartSeriesType SeriesType { get; }
```

## 例子

显示如何删除特定图表系列。

```csharp
Document doc = new Document(MyDir + "Reporting engine template - Chart series.docx");
Chart chart = ((Shape)doc.GetChild(NodeType.Shape, 0, true)).Chart;

// 删除所有列类型的系列。
for (int i = chart.Series.Count - 1; i >= 0; i--)
{
    if (chart.Series[i].SeriesType == ChartSeriesType.Column)
        chart.Series.RemoveAt(i);
}

chart.Series.Add(
    "Aspose Series",
    new string[] { "Category 1", "Category 2", "Category 3", "Category 4" },
    new double[] { 5.6, 7.1, 2.9, 8.9 });

doc.Save(ArtifactsDir + "Charts.RemoveSpecificChartSeries.docx");
```

### 也可以看看

* enum [ChartSeriesType](../../chartseriestype/)
* class [ChartSeries](../)
* 命名空间 [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* 部件 [Aspose.Words](../../../)
