---
title: ChartLegend.LegendEntries
second_title: Aspose.Words for .NET API 参考
description: ChartLegend 财产. 返回父图表的所有系列和趋势线的图例条目的集合
type: docs
weight: 10
url: /zh/net/aspose.words.drawing.charts/chartlegend/legendentries/
---
## ChartLegend.LegendEntries property

返回父图表的所有系列和趋势线的图例条目的集合。

```csharp
public ChartLegendEntryCollection LegendEntries { get; }
```

### 例子

展示如何使用图表系列的图例条目。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);

Chart chart = shape.Chart;
ChartSeriesCollection series = chart.Series;
series.Clear();

string[] categories = new string[] { "AW Category 1", "AW Category 2" };

ChartSeries series1 = series.Add("Series 1", categories, new double[] { 1, 2 });
series.Add("Series 2", categories, new double[] { 3, 4 });
series.Add("Series 3", categories, new double[] { 5, 6 });
series.Add("Series 4", categories, new double[] { 0, 0 });

ChartLegendEntryCollection legendEntries = chart.Legend.LegendEntries;
legendEntries[3].IsHidden = true;

foreach (ChartLegendEntry legendEntry in legendEntries)
    legendEntry.Font.Size = 12;

series1.LegendEntry.Font.Italic = true;

doc.Save(ArtifactsDir + "Charts.LegendEntries.docx");
```

### 也可以看看

* class [ChartLegendEntryCollection](../../chartlegendentrycollection/)
* class [ChartLegend](../)
* 命名空间 [Aspose.Words.Drawing.Charts](../../chartlegend/)
* 部件 [Aspose.Words](../../../)


