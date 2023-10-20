---
title: ChartLegendEntry.IsHidden
linktitle: IsHidden
articleTitle: IsHidden
second_title: 用于 .NET 的 Aspose.Words
description: ChartLegendEntry IsHidden 财产. 获取或设置一个值指示此条目是否隐藏在图表图例中 默认值为错误的 在 C#.
type: docs
weight: 20
url: /zh/net/aspose.words.drawing.charts/chartlegendentry/ishidden/
---
## ChartLegendEntry.IsHidden property

获取或设置一个值，指示此条目是否隐藏在图表图例中。 默认值为**错误的**.

```csharp
public bool IsHidden { get; set; }
```

## 评论

隐藏图表图例条目时，不会影响 仍显示在图表上的相应图表系列或趋势线。

## 例子

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

* class [ChartLegendEntry](../)
* 命名空间 [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* 部件 [Aspose.Words](../../../)
