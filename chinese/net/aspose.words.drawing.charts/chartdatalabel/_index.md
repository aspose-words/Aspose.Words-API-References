---
title: ChartDataLabel Class
linktitle: ChartDataLabel
articleTitle: ChartDataLabel
second_title: 用于 .NET 的 Aspose.Words
description: Aspose.Words.Drawing.Charts.ChartDataLabel 班级. 表示图表点或趋势线上的数据标签 在 C#.
type: docs
weight: 670
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
| [Index](../../aspose.words.drawing.charts/chartdatalabel/index/) { get; } | 指定包含元素的索引。 该索引应确定该元素适用于父集合的哪个子集合。 默认值为 0。 |
| [IsHidden](../../aspose.words.drawing.charts/chartdatalabel/ishidden/) { get; set; } | 获取/设置一个标志，指示该标签是否隐藏。 默认值为`错误的`. |
| [IsVisible](../../aspose.words.drawing.charts/chartdatalabel/isvisible/) { get; } | 返回`真的`如果此数据标签有要显示的内容。 |
| [NumberFormat](../../aspose.words.drawing.charts/chartdatalabel/numberformat/) { get; } | 返回父元素的数字格式。 |
| [Separator](../../aspose.words.drawing.charts/chartdatalabel/separator/) { get; set; } | 获取或设置用于图表上数据标签的字符串分隔符。 默认为逗号，但饼图仅显示类别名称和百分比时除外，此时应使用换行符 。 |
| [ShowBubbleSize](../../aspose.words.drawing.charts/chartdatalabel/showbubblesize/) { get; set; } | 允许指定是否为图表上的数据标签显示气泡大小。 仅适用于气泡图。 默认值为`错误的`. |
| [ShowCategoryName](../../aspose.words.drawing.charts/chartdatalabel/showcategoryname/) { get; set; } | 允许指定是否为图表上的数据标签显示类别名称。 默认值为`错误的`. |
| [ShowDataLabelsRange](../../aspose.words.drawing.charts/chartdatalabel/showdatalabelsrange/) { get; set; } | 允许指定数据标签范围内的值是否显示在数据标签中。 默认值为`错误的`. |
| [ShowLeaderLines](../../aspose.words.drawing.charts/chartdatalabel/showleaderlines/) { get; set; } | 允许指定是否需要显示数据标签引导线。 默认值为`错误的`. |
| [ShowLegendKey](../../aspose.words.drawing.charts/chartdatalabel/showlegendkey/) { get; set; } | 允许指定是否为图表上的数据标签显示图例键。 默认值为`错误的`. |
| [ShowPercentage](../../aspose.words.drawing.charts/chartdatalabel/showpercentage/) { get; set; } | 允许指定是否为图表上的数据标签显示百分比值。 默认值为`错误的`. |
| [ShowSeriesName](../../aspose.words.drawing.charts/chartdatalabel/showseriesname/) { get; set; } | 返回或设置一个布尔值以指示图表上数据标签的系列名称显示行为。 `真的`显示系列名称；`错误的`隐藏。默认情况下`错误的`. |
| [ShowValue](../../aspose.words.drawing.charts/chartdatalabel/showvalue/) { get; set; } | 允许指定值是否显示在数据标签中。 默认值为`错误的`. |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [ClearFormat](../../aspose.words.drawing.charts/chartdatalabel/clearformat/)() | 清除该数据标签的格式。这些属性设置为父 data 标签集合中定义的默认值。 |

## 评论

在一个系列中，`ChartDataLabel`对象是一个成员[`ChartDataLabelCollection`](../chartdatalabelcollection/)。 的[`ChartDataLabelCollection`](../chartdatalabelcollection/)包含一个`ChartDataLabel`每个点的对象。

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

* 命名空间 [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* 部件 [Aspose.Words](../../)
