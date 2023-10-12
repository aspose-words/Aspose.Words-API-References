---
title: ChartLegendEntry.Font
second_title: Aspose.Words for .NET API 参考
description: ChartLegendEntry 财产. 提供对此图例条目的字体格式的访问
type: docs
weight: 10
url: /zh/net/aspose.words.drawing.charts/chartlegendentry/font/
---
## ChartLegendEntry.Font property

提供对此图例条目的字体格式的访问。

```csharp
public Font Font { get; }
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

* class [Font](../../../aspose.words/font/)
* class [ChartLegendEntry](../)
* 命名空间 [Aspose.Words.Drawing.Charts](../../chartlegendentry/)
* 部件 [Aspose.Words](../../../)


