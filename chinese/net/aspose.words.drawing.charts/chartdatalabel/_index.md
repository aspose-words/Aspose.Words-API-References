---
title: Class ChartDataLabel
second_title: Aspose.Words for .NET API 参考
description: Aspose.Words.Drawing.Charts.ChartDataLabel 班级. 表示图表点或趋势线上的数据标签
type: docs
weight: 630
url: /zh/net/aspose.words.drawing.charts/chartdatalabel/
---
## ChartDataLabel class

表示图表点或趋势线上的数据标签。

```csharp
public class ChartDataLabel
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [Index](../../aspose.words.drawing.charts/chartdatalabel/index/) { get; } | 指定包含元素的索引。 此索引应确定此元素适用于哪个父子集合。 默认值为 0. |
| [IsHidden](../../aspose.words.drawing.charts/chartdatalabel/ishidden/) { get; set; } | 获取/设置一个标志，指示此标签是否隐藏。 默认值为 **错误的**. |
| [IsVisible](../../aspose.words.drawing.charts/chartdatalabel/isvisible/) { get; } | 如果此数据标签有要显示的内容，则返回 true。 |
| [NumberFormat](../../aspose.words.drawing.charts/chartdatalabel/numberformat/) { get; } | 返回父元素的数字格式。 |
| [Separator](../../aspose.words.drawing.charts/chartdatalabel/separator/) { get; set; } | 获取或设置用于图表数据标签的字符串分隔符。 默认为逗号，除了仅显示类别名称和百分比的饼图外，应使用换行符 。 |
| [ShowBubbleSize](../../aspose.words.drawing.charts/chartdatalabel/showbubblesize/) { get; set; } | 允许指定是否要为图表上的数据标签显示气泡大小。 仅适用于气泡图。 默认值为假。 |
| [ShowCategoryName](../../aspose.words.drawing.charts/chartdatalabel/showcategoryname/) { get; set; } | 允许指定是否为图表上的数据标签显示类别名称。 默认值为假。 |
| [ShowDataLabelsRange](../../aspose.words.drawing.charts/chartdatalabel/showdatalabelsrange/) { get; set; } | 允许指定数据标签范围内的值是否显示在数据标签中。 默认值为假。 |
| [ShowLeaderLines](../../aspose.words.drawing.charts/chartdatalabel/showleaderlines/) { get; set; } | 允许指定是否需要显示数据标签引导线。 默认值为假。 |
| [ShowLegendKey](../../aspose.words.drawing.charts/chartdatalabel/showlegendkey/) { get; set; } | 允许指定是否为图表上的数据标签显示图例键。 默认值为假。 |
| [ShowPercentage](../../aspose.words.drawing.charts/chartdatalabel/showpercentage/) { get; set; } | 允许指定是否为图表上的数据标签显示百分比值。 默认值为假。 |
| [ShowSeriesName](../../aspose.words.drawing.charts/chartdatalabel/showseriesname/) { get; set; } | 返回或设置一个布尔值以指示图表上数据标签的系列名称显示行为。 True 显示系列名称。虚假隐藏。默认为 false. |
| [ShowValue](../../aspose.words.drawing.charts/chartdatalabel/showvalue/) { get; set; } | 允许指定值是否显示在数据标签中。 默认值为假。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [ClearFormat](../../aspose.words.drawing.charts/chartdatalabel/clearformat/)() | 清除此数据标签的格式。属性设置为父 data 标签集合中定义的默认值。 |

### 评论

在一个系列中，`ChartDataLabel`对象是[`ChartDataLabelCollection`](../chartdatalabelcollection/) 的[`ChartDataLabelCollection`](../chartdatalabelcollection/)包含一个`ChartDataLabel`每个点的对象。

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

* 命名空间 [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* 部件 [Aspose.Words](../../)


