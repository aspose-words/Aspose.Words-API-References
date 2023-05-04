---
title: ChartDataLabelCollection Class
linktitle: ChartDataLabelCollection
articleTitle: ChartDataLabelCollection
second_title: Aspose.Words for .NET
description: Aspose.Words.Drawing.Charts.ChartDataLabelCollection class. Represents a collection of ChartDataLabel in C#.
type: docs
weight: 660
url: /net/aspose.words.drawing.charts/chartdatalabelcollection/
---
## ChartDataLabelCollection class

Represents a collection of [`ChartDataLabel`](../chartdatalabel/).

To learn more, visit the [Working with Charts](https://docs.aspose.com/words/net/working-with-charts/) documentation article.

```csharp
public class ChartDataLabelCollection : IEnumerable<ChartDataLabel>
```

## Properties

| Name | Description |
| --- | --- |
| [Count](../../aspose.words.drawing.charts/chartdatalabelcollection/count/) { get; } | Returns the number of [`ChartDataLabel`](../chartdatalabel/) in this collection. |
| [Font](../../aspose.words.drawing.charts/chartdatalabelcollection/font/) { get; } | Provides access to the font formatting of the data labels of the entire series. |
| [Item](../../aspose.words.drawing.charts/chartdatalabelcollection/item/) { get; } | Returns [`ChartDataLabel`](../chartdatalabel/) for the specified index. |
| [NumberFormat](../../aspose.words.drawing.charts/chartdatalabelcollection/numberformat/) { get; } | Gets an [`ChartNumberFormat`](../chartnumberformat/) instance allowing to set number format for the data labels of the entire series. |
| [Separator](../../aspose.words.drawing.charts/chartdatalabelcollection/separator/) { get; set; } | Gets or sets string separator used for the data labels of the entire series. The default is a comma, except for pie charts showing only category name and percentage, when a line break shall be used instead. |
| [ShowBubbleSize](../../aspose.words.drawing.charts/chartdatalabelcollection/showbubblesize/) { get; set; } | Allows to specify whether bubble size is to be displayed for the data labels of the entire series. Applies only to Bubble charts. Default value is `false`. |
| [ShowCategoryName](../../aspose.words.drawing.charts/chartdatalabelcollection/showcategoryname/) { get; set; } | Allows to specify whether category name is to be displayed for the data labels of the entire series. Default value is `false`. |
| [ShowDataLabelsRange](../../aspose.words.drawing.charts/chartdatalabelcollection/showdatalabelsrange/) { get; set; } | Allows to specify whether values from data labels range to be displayed in the data labels of the entire series. Default value is `false`. |
| [ShowLeaderLines](../../aspose.words.drawing.charts/chartdatalabelcollection/showleaderlines/) { get; set; } | Allows to specify whether data label leader lines need be shown for the data labels of the entire series. Default value is `false`. |
| [ShowLegendKey](../../aspose.words.drawing.charts/chartdatalabelcollection/showlegendkey/) { get; set; } | Allows to specify whether legend key is to be displayed for the data labels of the entire series. Default value is `false`. |
| [ShowPercentage](../../aspose.words.drawing.charts/chartdatalabelcollection/showpercentage/) { get; set; } | Allows to specify whether percentage value is to be displayed for the data labels of the entire series. Default value is `false`. Applies only to Pie charts. |
| [ShowSeriesName](../../aspose.words.drawing.charts/chartdatalabelcollection/showseriesname/) { get; set; } | Returns or sets a Boolean to indicate the series name display behavior for the data labels of the entire series. `true` to show the series name; `false` to hide. By default `false`. |
| [ShowValue](../../aspose.words.drawing.charts/chartdatalabelcollection/showvalue/) { get; set; } | Allows to specify whether values are to be displayed in the data labels of the entire series. Default value is `false`. |

## Methods

| Name | Description |
| --- | --- |
| [ClearFormat](../../aspose.words.drawing.charts/chartdatalabelcollection/clearformat/)() | Clears format of all [`ChartDataLabel`](../chartdatalabel/) in this collection. |
| [GetEnumerator](../../aspose.words.drawing.charts/chartdatalabelcollection/getenumerator/)() | Returns an enumerator object. |

## Examples

Shows how to apply labels to data points in a line chart.

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

    // Apply data labels to every series in the chart.
    // These labels will appear next to each data point in the graph and display its value.
    foreach (ChartSeries series in chart.Series)
    {
        ApplyDataLabels(series, 4, "000.0", ", ");
        Assert.AreEqual(4, series.DataLabels.Count);
    }

    // Change the separator string for every data label in a series.
    using (IEnumerator<ChartDataLabel> enumerator = chart.Series[0].DataLabels.GetEnumerator())
    {
        while (enumerator.MoveNext())
        {
            Assert.AreEqual(", ", enumerator.Current.Separator);
            enumerator.Current.Separator = " & ";
        }
    }

    // For a cleaner looking graph, we can remove data labels individually.
    chart.Series[1].DataLabels[2].ClearFormat();

    // We can also strip an entire series of its data labels at once.
    chart.Series[2].DataLabels.ClearFormat();

    doc.Save(ArtifactsDir + "Charts.DataLabels.docx");
}

/// <summary>
/// Apply data labels with custom number format and separator to several data points in a series.
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

### See Also

* class [ChartDataLabel](../chartdatalabel/)
* namespace [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* assembly [Aspose.Words](../../)
