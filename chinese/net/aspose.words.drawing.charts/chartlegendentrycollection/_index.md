---
title: Class ChartLegendEntryCollection
second_title: Aspose.Words for .NET API 参考
description: Aspose.Words.Drawing.Charts.ChartLegendEntryCollection 班级. 表示图表图例条目的集合
type: docs
weight: 740
url: /zh/net/aspose.words.drawing.charts/chartlegendentrycollection/
---
## ChartLegendEntryCollection class

表示图表图例条目的集合。

要了解更多信息，请访问[使用图表](https://docs.aspose.com/words/net/working-with-charts/)文档文章。

```csharp
public class ChartLegendEntryCollection : IEnumerable<ChartLegendEntry>
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [Count](../../aspose.words.drawing.charts/chartlegendentrycollection/count/) { get; } | 返回数量[`ChartLegendEntry`](../chartlegendentry/)在这个集合中. |
| [Item](../../aspose.words.drawing.charts/chartlegendentrycollection/item/) { get; } | 返回[`ChartLegendEntry`](../chartlegendentry/)对于指定的索引. |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [GetEnumerator](../../aspose.words.drawing.charts/chartlegendentrycollection/getenumerator/)() | 返回一个枚举器对象。 |

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

* class [ChartLegendEntry](../chartlegendentry/)
* 命名空间 [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* 部件 [Aspose.Words](../../)


