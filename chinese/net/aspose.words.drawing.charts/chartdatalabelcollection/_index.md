---
title: ChartDataLabelCollection
second_title: Aspose.Words for .NET API 参考
description: 代表一个集合ChartDataLabel./chartdatalabel.
type: docs
weight: 640
url: /zh/net/aspose.words.drawing.charts/chartdatalabelcollection/
---
## ChartDataLabelCollection class

代表一个集合[`ChartDataLabel`](../chartdatalabel).

```csharp
public class ChartDataLabelCollection : IEnumerable<ChartDataLabel>
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [Count](../../aspose.words.drawing.charts/chartdatalabelcollection/count) { get; } | 返回数量[`ChartDataLabel`](../chartdatalabel)在这个集合中。 |
| [Item](../../aspose.words.drawing.charts/chartdatalabelcollection/item) { get; } | 返回[`ChartDataLabel`](../chartdatalabel)对于指定的索引。 |
| [NumberFormat](../../aspose.words.drawing.charts/chartdatalabelcollection/numberformat) { get; } | 得到一个[`ChartNumberFormat`](../chartnumberformat)允许为 the 整个系列的数据标签设置数字格式的实例。 |
| [Separator](../../aspose.words.drawing.charts/chartdatalabelcollection/separator) { get; set; } | 获取或设置用于整个系列数据标签的字符串分隔符。 默认为逗号，除了仅显示类别名称和百分比的饼图外，应使用换行符 。 |
| [ShowBubbleSize](../../aspose.words.drawing.charts/chartdatalabelcollection/showbubblesize) { get; set; } | 允许指定是否为整个系列的数据标签显示气泡大小。 仅适用于气泡图。 默认值为 **错误的**. |
| [ShowCategoryName](../../aspose.words.drawing.charts/chartdatalabelcollection/showcategoryname) { get; set; } | 允许指定是否为整个系列的数据标签显示类别名称。 默认值为 **错误的**. |
| [ShowDataLabelsRange](../../aspose.words.drawing.charts/chartdatalabelcollection/showdatalabelsrange) { get; set; } | 允许指定数据标签范围内的值是否显示在整个系列的数据标签中。 默认值为 **错误的**. |
| [ShowLeaderLines](../../aspose.words.drawing.charts/chartdatalabelcollection/showleaderlines) { get; set; } | 允许指定是否需要为整个系列的数据标签显示数据标签引出线。 默认值为 **错误的**. |
| [ShowLegendKey](../../aspose.words.drawing.charts/chartdatalabelcollection/showlegendkey) { get; set; } | 允许指定是否为整个系列的数据标签显示图例键。 默认值为 **错误的**. |
| [ShowPercentage](../../aspose.words.drawing.charts/chartdatalabelcollection/showpercentage) { get; set; } | 允许指定是否为整个系列的数据标签显示百分比值。 默认值为 **错误的**.仅适用于饼图。 |
| [ShowSeriesName](../../aspose.words.drawing.charts/chartdatalabelcollection/showseriesname) { get; set; } | 返回或设置一个布尔值，表示整个系列的数据标签的系列名称显示行为。  **真的**显示系列名称。 **错误的**隐藏。默认 **错误的**. |
| [ShowValue](../../aspose.words.drawing.charts/chartdatalabelcollection/showvalue) { get; set; } | 允许指定是否在整个系列的数据标签中显示值。 默认值为 **错误的**. |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [ClearFormat](../../aspose.words.drawing.charts/chartdatalabelcollection/clearformat)() | 清除所有格式[`ChartDataLabel`](../chartdatalabel)在这个集合中。 |
| [GetEnumerator](../../aspose.words.drawing.charts/chartdatalabelcollection/getenumerator)() | 返回一个枚举器对象。 |

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

* class [ChartDataLabel](../chartdatalabel)
* 命名空间 [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts)
* 部件 [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
