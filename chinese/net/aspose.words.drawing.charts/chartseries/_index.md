---
title: ChartSeries Class
linktitle: ChartSeries
articleTitle: ChartSeries
second_title: 用于 .NET 的 Aspose.Words
description: Aspose.Words.Drawing.Charts.ChartSeries 班级. 代表图表系列属性 在 C#.
type: docs
weight: 780
url: /zh/net/aspose.words.drawing.charts/chartseries/
---
## ChartSeries class

代表图表系列属性。

要了解更多信息，请访问[使用图表](https://docs.aspose.com/words/net/working-with-charts/)文档文章。

```csharp
public class ChartSeries : IChartDataPoint
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [Bubble3D](../../aspose.words.drawing.charts/chartseries/bubble3d/) { get; set; } | 指定气泡图中的气泡是否应应用 3-D 效果。 |
| [BubbleSizes](../../aspose.words.drawing.charts/chartseries/bubblesizes/) { get; } | 获取此图表系列的气泡大小的集合。 |
| [DataLabels](../../aspose.words.drawing.charts/chartseries/datalabels/) { get; } | 指定整个系列的数据标签的设置。 |
| [DataPoints](../../aspose.words.drawing.charts/chartseries/datapoints/) { get; } | 返回该系列中所有数据点的格式化对象的集合。 |
| [Explosion](../../aspose.words.drawing.charts/chartseries/explosion/) { get; set; } | 指定数据点应从饼图中心移动的量。 可以为负数，负数表示未设置属性且不应应用爆炸。 仅适用于饼图。 |
| [Format](../../aspose.words.drawing.charts/chartseries/format/) { get; } | 提供对系列的填充和线条格式的访问。 |
| [HasDataLabels](../../aspose.words.drawing.charts/chartseries/hasdatalabels/) { get; set; } | 获取或设置一个标志，指示是否显示该系列的数据标签。 |
| [InvertIfNegative](../../aspose.words.drawing.charts/chartseries/invertifnegative/) { get; set; } | 指定如果值为负数，父元素是否应反转其颜色。 |
| [LegendEntry](../../aspose.words.drawing.charts/chartseries/legendentry/) { get; } | 获取此图表系列的图例条目。 |
| [Marker](../../aspose.words.drawing.charts/chartseries/marker/) { get; } | 指定数据标记。根据请求自动创建标记。 |
| [Name](../../aspose.words.drawing.charts/chartseries/name/) { get; set; } | 获取或设置系列的名称，如果未显式设置名称，则使用索引生成。 默认情况下返回系列加一的索引。 |
| [SeriesType](../../aspose.words.drawing.charts/chartseries/seriestype/) { get; } | 获取此图表系列的类型。 |
| [Smooth](../../aspose.words.drawing.charts/chartseries/smooth/) { get; set; } | 允许指定是否应使用 Catmull-Rom 样条线来平滑连接图表上的点的线。 |
| [XValues](../../aspose.words.drawing.charts/chartseries/xvalues/) { get; } | 获取此图表系列的 X 值的集合。 |
| [YValues](../../aspose.words.drawing.charts/chartseries/yvalues/) { get; } | 获取此图表系列的 Y 值集合。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [Add](../../aspose.words.drawing.charts/chartseries/add/#add)(*[ChartXValue](../chartxvalue/)*) | 将指定的 X 值添加到图表系列。如果该系列支持 Y 值和气泡大小，它们将为 X 值 留空。 |
| [Add](../../aspose.words.drawing.charts/chartseries/add/#add_1)(*[ChartXValue](../chartxvalue/), [ChartYValue](../chartyvalue/)*) | 将指定的 X 和 Y 值添加到图表系列。 |
| [Add](../../aspose.words.drawing.charts/chartseries/add/#add_2)(*[ChartXValue](../chartxvalue/), [ChartYValue](../chartyvalue/), double*) | 将指定的 X 值、Y 值和气泡大小添加到图表系列中。 |
| [Clear](../../aspose.words.drawing.charts/chartseries/clear/)() | 从图表系列中删除所有数据值。所有单独数据点和数据标签的格式均已清除。 |
| [ClearValues](../../aspose.words.drawing.charts/chartseries/clearvalues/)() | 从图表系列中删除所有数据值，并保留数据点和数据标签的格式。 |
| [Insert](../../aspose.words.drawing.charts/chartseries/insert/#insert)(*int, [ChartXValue](../chartxvalue/)*) | 将指定的 X 值插入到图表系列的指定索引处。如果系列支持 Y 值 和气泡大小，则 X 值它们将为空。 |
| [Insert](../../aspose.words.drawing.charts/chartseries/insert/#insert_1)(*int, [ChartXValue](../chartxvalue/), [ChartYValue](../chartyvalue/)*) | 将指定的 X 和 Y 值插入图表系列中指定的索引处。 |
| [Insert](../../aspose.words.drawing.charts/chartseries/insert/#insert_2)(*int, [ChartXValue](../chartxvalue/), [ChartYValue](../chartyvalue/), double*) | 将指定的 X 值、Y 值和气泡大小插入到图表系列的指定索引处。 |
| [Remove](../../aspose.words.drawing.charts/chartseries/remove/)(*int*) | 从指定索引处的图表系列中删除 X 值、Y 值和气泡大小（如果支持）。 相应的数据点和数据标签也会被删除。 |

## 例子

展示如何将标签应用到折线图中的数据点。

```csharp
public void DataLabels()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    Shape chartShape = builder.InsertChart(ChartType.Line, 400, 300);
    Chart chart = chartShape.Chart;

    Assert.AreEqual(3, chart.Series.Count);
    Assert.AreEqual("Series 1", chart.Series[0].Name);
    Assert.AreEqual("Series 2", chart.Series[1].Name);
    Assert.AreEqual("Series 3", chart.Series[2].Name);

    // 将数据标签应用于图表中的每个系列。
    // 这些标签将出现在图表中每个数据点旁边并显示其值。
    foreach (ChartSeries series in chart.Series)
    {
        ApplyDataLabels(series, 4, "000.0", ", ");
        Assert.AreEqual(4, series.DataLabels.Count);
    }

    // 更改系列中每个数据标签的分隔符字符串。
    using (IEnumerator<ChartDataLabel> enumerator = chart.Series[0].DataLabels.GetEnumerator())
    {
        while (enumerator.MoveNext())
        {
            Assert.AreEqual(", ", enumerator.Current.Separator);
            enumerator.Current.Separator = " & ";
        }
    }

    // 为了使图表看起来更清晰，我们可以单独删除数据标签。
    chart.Series[1].DataLabels[2].ClearFormat();

    // 我们还可以一次剥离整个系列的数据标签。
    chart.Series[2].DataLabels.ClearFormat();

    doc.Save(ArtifactsDir + "Charts.DataLabels.docx");
}

/// <summary>
/// 将具有自定义数字格式和分隔符的数据标签应用于一系列中的多个数据点。
/// </summary>
private static void ApplyDataLabels(ChartSeries series, int labelsCount, string numberFormat, string separator)
{
    for (int i = 0; i < labelsCount; i++)
    {
        series.HasDataLabels = true;

        Assert.False(series.DataLabels[i].IsVisible);

        series.DataLabels[i].ShowCategoryName = true;
        series.DataLabels[i].ShowSeriesName = true;
        series.DataLabels[i].ShowValue = true;
        series.DataLabels[i].ShowLeaderLines = true;
        series.DataLabels[i].ShowLegendKey = true;
        series.DataLabels[i].ShowPercentage = false;
        series.DataLabels[i].IsHidden = false;
        Assert.False(series.DataLabels[i].ShowDataLabelsRange);

        series.DataLabels[i].NumberFormat.FormatCode = numberFormat;
        series.DataLabels[i].Separator = separator;

        Assert.False(series.DataLabels[i].ShowDataLabelsRange);
        Assert.True(series.DataLabels[i].IsVisible);
        Assert.False(series.DataLabels[i].IsHidden);
    }
}
```

### 也可以看看

* interface [IChartDataPoint](../ichartdatapoint/)
* 命名空间 [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* 部件 [Aspose.Words](../../)
