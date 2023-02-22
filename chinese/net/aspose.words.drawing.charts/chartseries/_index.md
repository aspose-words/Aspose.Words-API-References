---
title: Class ChartSeries
second_title: Aspose.Words for .NET API 参考
description: Aspose.Words.Drawing.Charts.ChartSeries 班级. 表示图表系列属性
type: docs
weight: 730
url: /zh/net/aspose.words.drawing.charts/chartseries/
---
## ChartSeries class

表示图表系列属性。

```csharp
public class ChartSeries : IChartDataPoint
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [Bubble3D](../../aspose.words.drawing.charts/chartseries/bubble3d/) { get; set; } |  |
| [DataLabels](../../aspose.words.drawing.charts/chartseries/datalabels/) { get; } | 指定整个系列的数据标签设置。 |
| [DataPoints](../../aspose.words.drawing.charts/chartseries/datapoints/) { get; } | 返回此系列中所有数据点的格式化对象集合。 |
| [Explosion](../../aspose.words.drawing.charts/chartseries/explosion/) { get; set; } |  |
| [Format](../../aspose.words.drawing.charts/chartseries/format/) { get; } | 提供对系列的填充和线条格式的访问。 |
| [HasDataLabels](../../aspose.words.drawing.charts/chartseries/hasdatalabels/) { get; set; } | 获取或设置是否为系列显示数据标签的标志。 |
| [InvertIfNegative](../../aspose.words.drawing.charts/chartseries/invertifnegative/) { get; set; } |  |
| [LegendEntry](../../aspose.words.drawing.charts/chartseries/legendentry/) { get; } | 获取此图表系列的图例条目。 |
| [Marker](../../aspose.words.drawing.charts/chartseries/marker/) { get; } |  |
| [Name](../../aspose.words.drawing.charts/chartseries/name/) { get; set; } | 获取或设置系列的名称，如果未明确设置名称，则使用索引生成。 默认情况下返回系列加一个基于索引。 |
| [Smooth](../../aspose.words.drawing.charts/chartseries/smooth/) { get; set; } | 允许指定连接图表上点的线是否应使用 Catmull-Rom 样条进行平滑。 |

### 例子

显示如何将标签应用于折线图中的数据点。

```csharp
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
    // 这些标签将出现在图表中每个数据点的旁边并显示其值。
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

    // 为了更清晰的图表，我们可以单独删除数据标签。
    chart.Series[1].DataLabels[2].ClearFormat();

    // 我们也可以一次剥离整个系列的数据标签。
    chart.Series[2].DataLabels.ClearFormat();

    doc.Save(ArtifactsDir + "Charts.DataLabels.docx");
}

/// <summary>
/// 将具有自定义数字格式和分隔符的数据标签应用于系列中的多个数据点。
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


