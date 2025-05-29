---
title: ChartDataLabel Class
linktitle: ChartDataLabel
articleTitle: ChartDataLabel
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Drawing.Charts.ChartDataLabel 类，增强图表数据可视化。使用精准的数据标签提升您的演示文稿！
type: docs
weight: 930
url: /zh/net/aspose.words.drawing.charts/chartdatalabel/
---
## ChartDataLabel class

表示图表点或趋势线上的数据标签。

要了解更多信息，请访问[使用图表](https://docs.aspose.com/words/net/working-with-charts/)文档文章。

```csharp
public class ChartDataLabel
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [Font](../../aspose.words.drawing.charts/chartdatalabel/font/) { get; } | 提供对此数据标签的字体格式的访问。 |
| [Format](../../aspose.words.drawing.charts/chartdatalabel/format/) { get; } | 提供对数据标签的填充和线条格式的访问。 |
| [Index](../../aspose.words.drawing.charts/chartdatalabel/index/) { get; } | 指定包含元素的索引。 此索引确定此元素适用于父级的哪个子集合。 默认值为 0。 |
| [IsHidden](../../aspose.words.drawing.charts/chartdatalabel/ishidden/) { get; set; } | 获取/设置一个标志，指示此标签是否隐藏。 默认值为`错误的`. |
| [IsVisible](../../aspose.words.drawing.charts/chartdatalabel/isvisible/) { get; } | 返回`真的`如果此数据标签有内容要显示。 |
| [Left](../../aspose.words.drawing.charts/chartdatalabel/left/) { get; set; } | 获取或设置数据标签与图表左边缘或其指定位置的距离（以点为单位）[`Position`](./position/)财产，取决于[`LeftMode`](./leftmode/) 属性. |
| [LeftMode](../../aspose.words.drawing.charts/chartdatalabel/leftmode/) { get; set; } | 获取或设置[`Left`](./left/)属性值：是否设置数据标签的 location 距离图表左边缘或距离其指定的位置[`Position`](./position/) 属性. |
| [NumberFormat](../../aspose.words.drawing.charts/chartdatalabel/numberformat/) { get; } | 返回父元素的数字格式。 |
| [Orientation](../../aspose.words.drawing.charts/chartdatalabel/orientation/) { get; set; } | 获取或设置标签文本的方向。 |
| [Position](../../aspose.words.drawing.charts/chartdatalabel/position/) { get; set; } | 获取或设置数据标签的位置。 |
| [Rotation](../../aspose.words.drawing.charts/chartdatalabel/rotation/) { get; set; } | 获取或设置标签的旋转角度（以度为单位）。 |
| [Separator](../../aspose.words.drawing.charts/chartdatalabel/separator/) { get; set; } | 获取或设置用于图表上数据标签的字符串分隔符。 默认值为逗号，但仅显示类别名称和百分比的饼图除外，此时应使用换行符 。 |
| [ShowBubbleSize](../../aspose.words.drawing.charts/chartdatalabel/showbubblesize/) { get; set; } | 允许指定是否在图表上显示数据标签的气泡大小。 仅适用于气泡图。 默认值为`错误的`. |
| [ShowCategoryName](../../aspose.words.drawing.charts/chartdatalabel/showcategoryname/) { get; set; } | 允许指定是否在图表上显示数据标签的类别名称。 默认值为`错误的`. |
| [ShowDataLabelsRange](../../aspose.words.drawing.charts/chartdatalabel/showdatalabelsrange/) { get; set; } | 允许指定数据标签范围内的值是否显示在数据标签中。 默认值为`错误的`. |
| [ShowLeaderLines](../../aspose.words.drawing.charts/chartdatalabel/showleaderlines/) { get; set; } | 允许指定是否需要显示数据标签引线。 默认值为`错误的`. |
| [ShowLegendKey](../../aspose.words.drawing.charts/chartdatalabel/showlegendkey/) { get; set; } | 允许指定是否在图表上显示数据标签的图例键。 默认值为`错误的`. |
| [ShowPercentage](../../aspose.words.drawing.charts/chartdatalabel/showpercentage/) { get; set; } | 允许指定是否在图表上的数据标签中显示百分比值。 默认值为`错误的`. |
| [ShowSeriesName](../../aspose.words.drawing.charts/chartdatalabel/showseriesname/) { get; set; } | 返回或设置一个布尔值来指示图表上数据标签的系列名称显示行为。 `真的`显示系列名称；`错误的`隐藏。默认情况下`错误的`. |
| [ShowValue](../../aspose.words.drawing.charts/chartdatalabel/showvalue/) { get; set; } | 允许指定是否在数据标签中显示值。 默认值为`错误的`. |
| [Top](../../aspose.words.drawing.charts/chartdatalabel/top/) { get; set; } | 获取或设置数据标签与图表顶部边缘或其指定位置的距离（以点为单位）[`Position`](./position/)财产，取决于[`TopMode`](./topmode/) 属性. |
| [TopMode](../../aspose.words.drawing.charts/chartdatalabel/topmode/) { get; set; } | 获取或设置[`Top`](./top/)属性值：是否设置数据标签的 location 距离图表顶部边缘或距离其指定的位置[`Position`](./position/) 属性. |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [ClearFormat](../../aspose.words.drawing.charts/chartdatalabel/clearformat/)() | 清除此数据标签的格式。属性设置为父数据 标签集合中定义的默认值。 |

## 评论

在一个系列中，`ChartDataLabel`对象是[`ChartDataLabelCollection`](../chartdatalabelcollection/) 该[`ChartDataLabelCollection`](../chartdatalabelcollection/)包含一个`ChartDataLabel`每个点的对象。

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

* 命名空间 [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* 部件 [Aspose.Words](../../)
