---
title: ChartSeries Class
linktitle: ChartSeries
articleTitle: ChartSeries
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Drawing.Charts.ChartSeries 类，这是增强动态文档创建和可视化的图表系列属性的关键。
type: docs
weight: 1070
url: /zh/net/aspose.words.drawing.charts/chartseries/
---
## ChartSeries class

表示图表系列属性。

要了解更多信息，请访问[使用图表](https://docs.aspose.com/words/net/working-with-charts/)文档文章。

```csharp
public class ChartSeries : IChartDataPoint
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [Bubble3D](../../aspose.words.drawing.charts/chartseries/bubble3d/) { get; set; } | 指定气泡图中的气泡是否应用三维效果。 |
| [BubbleSizes](../../aspose.words.drawing.charts/chartseries/bubblesizes/) { get; } | 获取此图表系列的气泡大小集合。 |
| [DataLabels](../../aspose.words.drawing.charts/chartseries/datalabels/) { get; } | 指定整个系列的数据标签设置。 |
| [DataPoints](../../aspose.words.drawing.charts/chartseries/datapoints/) { get; } | 返回此系列中所有数据点的格式化对象集合。 |
| [Explosion](../../aspose.words.drawing.charts/chartseries/explosion/) { get; set; } | 指定数据点应从饼图中心移动的量。 可以为负数，负数表示未设置属性，不应应用爆炸。 仅适用于饼图。 |
| [Format](../../aspose.words.drawing.charts/chartseries/format/) { get; } | 提供对系列填充和线条格式的访问。 |
| [HasDataLabels](../../aspose.words.drawing.charts/chartseries/hasdatalabels/) { get; set; } | 获取或设置一个标志，指示是否显示系列的数据标签。 |
| [InvertIfNegative](../../aspose.words.drawing.charts/chartseries/invertifnegative/) { get; set; } | 指定当值为负时父元素是否应反转其颜色。 |
| [LegendEntry](../../aspose.words.drawing.charts/chartseries/legendentry/) { get; } | 获取此图表系列的图例条目。 |
| [Marker](../../aspose.words.drawing.charts/chartseries/marker/) { get; } | 指定数据标记。请求时会自动创建标记。 |
| [Name](../../aspose.words.drawing.charts/chartseries/name/) { get; set; } | 获取或设置系列的名称，如果未明确设置名称，则使用索引生成。 默认情况下返回系列加上一个基于索引的索引。 |
| [SeriesType](../../aspose.words.drawing.charts/chartseries/seriestype/) { get; } | 获取此图表系列的类型。 |
| [Smooth](../../aspose.words.drawing.charts/chartseries/smooth/) { get; set; } | 允许指定是否使用 Catmull-Rom 样条曲线对图表上各点之间的连接线进行平滑处理。 |
| [XValues](../../aspose.words.drawing.charts/chartseries/xvalues/) { get; } | 获取此图表系列的 X 值集合。 |
| [YValues](../../aspose.words.drawing.charts/chartseries/yvalues/) { get; } | 获取此图表系列的 Y 值集合。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [Add](../../aspose.words.drawing.charts/chartseries/add/#add)(*[ChartXValue](../chartxvalue/)*) | 将指定的 X 值添加到图表系列。如果该系列支持 Y 值和气泡大小，则 X 值将为空。 |
| [Add](../../aspose.words.drawing.charts/chartseries/add/#add_1)(*[ChartXValue](../chartxvalue/), [ChartYValue](../chartyvalue/)*) | 将指定的 X 和 Y 值添加到图表系列。 |
| [Add](../../aspose.words.drawing.charts/chartseries/add/#add_2)(*[ChartXValue](../chartxvalue/), [ChartYValue](../chartyvalue/), double*) | 将指定的 X 值、Y 值和气泡大小添加到图表系列。 |
| [Clear](../../aspose.words.drawing.charts/chartseries/clear/)() | 从图表系列中删除所有数据值。所有单个数据点和数据标签的格式均被清除。 |
| [ClearValues](../../aspose.words.drawing.charts/chartseries/clearvalues/)() | 从图表系列中删除所有数据值，同时保留数据点和数据标签的格式。 |
| [CopyFormatFrom](../../aspose.words.drawing.charts/chartseries/copyformatfrom/)(*int*) | 从具有指定索引的数据点复制默认数据点格式。 |
| [Insert](../../aspose.words.drawing.charts/chartseries/insert/#insert)(*int, [ChartXValue](../chartxvalue/)*) | 将指定的 X 值插入图表系列的指定索引处。如果该系列支持 Y 值和气泡大小，则 X 值将为空。 |
| [Insert](../../aspose.words.drawing.charts/chartseries/insert/#insert_1)(*int, [ChartXValue](../chartxvalue/), [ChartYValue](../chartyvalue/)*) | 将指定的 X 和 Y 值插入到指定索引处的图表系列中。 |
| [Insert](../../aspose.words.drawing.charts/chartseries/insert/#insert_2)(*int, [ChartXValue](../chartxvalue/), [ChartYValue](../chartyvalue/), double*) | 将指定的 X 值、Y 值和气泡大小插入到指定索引处的图表系列中。 |
| [Remove](../../aspose.words.drawing.charts/chartseries/remove/)(*int*) | 从指定索引处的图表系列中删除 X 值、Y 值和气泡大小（如果支持）。 相应的数据点和数据标签也将被删除。 |

## 例子

展示如何将标签应用于折线图中的数据点。

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

    ChartDataLabel dataLabel = chart.Series[1].DataLabels[2];
    dataLabel.Format.Fill.Color = Color.Red;

    // 为了使图表看起来更清晰，我们可以单独删除数据标签。
    dataLabel.ClearFormat();

    // 我们还可以一次性剥离整个系列的数据标签。
    chart.Series[2].DataLabels.ClearFormat();

    doc.Save(ArtifactsDir + "Charts.DataLabels.docx");
}

/// <summary>
/// 将具有自定义数字格式和分隔符的数据标签应用于一系列中的多个数据点。
/// </summary>
private static void ApplyDataLabels(ChartSeries series, int labelsCount, string numberFormat, string separator)
{
    series.HasDataLabels = true;
    series.Explosion = 40;

    for (int i = 0; i < labelsCount; i++)
    {
        Assert.False(series.DataLabels[i].IsVisible);

        series.DataLabels[i].ShowCategoryName = true;
        series.DataLabels[i].ShowSeriesName = true;
        series.DataLabels[i].ShowValue = true;
        series.DataLabels[i].ShowLeaderLines = true;
        series.DataLabels[i].ShowLegendKey = true;
        series.DataLabels[i].ShowPercentage = false;
        Assert.False(series.DataLabels[i].IsHidden);
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
