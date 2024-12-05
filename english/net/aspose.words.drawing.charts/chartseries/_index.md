---
title: ChartSeries Class
linktitle: ChartSeries
articleTitle: ChartSeries
second_title: Aspose.Words for .NET
description: Aspose.Words.Drawing.Charts.ChartSeries class. Represents chart series properties in C#.
type: docs
weight: 1050
url: /net/aspose.words.drawing.charts/chartseries/
---
## ChartSeries class

Represents chart series properties.

To learn more, visit the [Working with Charts](https://docs.aspose.com/words/net/working-with-charts/) documentation article.

```csharp
public class ChartSeries : IChartDataPoint
```

## Properties

| Name | Description |
| --- | --- |
| [Bubble3D](../../aspose.words.drawing.charts/chartseries/bubble3d/) { get; set; } | Specifies whether the bubbles in Bubble chart should have a 3-D effect applied to them. |
| [BubbleSizes](../../aspose.words.drawing.charts/chartseries/bubblesizes/) { get; } | Gets a collection of bubble sizes for this chart series. |
| [DataLabels](../../aspose.words.drawing.charts/chartseries/datalabels/) { get; } | Specifies the settings for the data labels for the entire series. |
| [DataPoints](../../aspose.words.drawing.charts/chartseries/datapoints/) { get; } | Returns a collection of formatting objects for all data points in this series. |
| [Explosion](../../aspose.words.drawing.charts/chartseries/explosion/) { get; set; } | Specifies the amount the data point shall be moved from the center of the pie. Can be negative, negative means that property is not set and no explosion should be applied. Applies only to Pie charts. |
| [Format](../../aspose.words.drawing.charts/chartseries/format/) { get; } | Provides access to fill and line formatting of the series. |
| [HasDataLabels](../../aspose.words.drawing.charts/chartseries/hasdatalabels/) { get; set; } | Gets or sets a flag indicating whether data labels are displayed for the series. |
| [InvertIfNegative](../../aspose.words.drawing.charts/chartseries/invertifnegative/) { get; set; } | Specifies whether the parent element shall inverts its colors if the value is negative. |
| [LegendEntry](../../aspose.words.drawing.charts/chartseries/legendentry/) { get; } | Gets a legend entry for this chart series. |
| [Marker](../../aspose.words.drawing.charts/chartseries/marker/) { get; } | Specifies a data marker. Marker is automatically created when requested. |
| [Name](../../aspose.words.drawing.charts/chartseries/name/) { get; set; } | Gets or sets the name of the series, if name is not set explicitly it is generated using index. By default returns Series plus one based index. |
| [SeriesType](../../aspose.words.drawing.charts/chartseries/seriestype/) { get; } | Gets the type of this chart series. |
| [Smooth](../../aspose.words.drawing.charts/chartseries/smooth/) { get; set; } | Allows to specify whether the line connecting the points on the chart shall be smoothed using Catmull-Rom splines. |
| [XValues](../../aspose.words.drawing.charts/chartseries/xvalues/) { get; } | Gets a collection of X values for this chart series. |
| [YValues](../../aspose.words.drawing.charts/chartseries/yvalues/) { get; } | Gets a collection of Y values for this chart series. |

## Methods

| Name | Description |
| --- | --- |
| [Add](../../aspose.words.drawing.charts/chartseries/add/#add)(*[ChartXValue](../chartxvalue/)*) | Adds the specified X value to the chart series. If the series supports Y values and bubble sizes, they will be empty for the X value. |
| [Add](../../aspose.words.drawing.charts/chartseries/add/#add_1)(*[ChartXValue](../chartxvalue/), [ChartYValue](../chartyvalue/)*) | Adds the specified X and Y values to the chart series. |
| [Add](../../aspose.words.drawing.charts/chartseries/add/#add_2)(*[ChartXValue](../chartxvalue/), [ChartYValue](../chartyvalue/), double*) | Adds the specified X value, Y value and bubble size to the chart series. |
| [Clear](../../aspose.words.drawing.charts/chartseries/clear/)() | Removes all data values from the chart series. Format of all individual data points and data labels is cleared. |
| [ClearValues](../../aspose.words.drawing.charts/chartseries/clearvalues/)() | Removes all data values from the chart series with preserving the format of the data points and data labels. |
| [CopyFormatFrom](../../aspose.words.drawing.charts/chartseries/copyformatfrom/)(*int*) | Copies default data point format from the data point with the specified index. |
| [Insert](../../aspose.words.drawing.charts/chartseries/insert/#insert)(*int, [ChartXValue](../chartxvalue/)*) | Inserts the specified X value into the chart series at the specified index. If the series supports Y values and bubble sizes, they will be empty for the X value. |
| [Insert](../../aspose.words.drawing.charts/chartseries/insert/#insert_1)(*int, [ChartXValue](../chartxvalue/), [ChartYValue](../chartyvalue/)*) | Inserts the specified X and Y values into the chart series at the specified index. |
| [Insert](../../aspose.words.drawing.charts/chartseries/insert/#insert_2)(*int, [ChartXValue](../chartxvalue/), [ChartYValue](../chartyvalue/), double*) | Inserts the specified X value, Y value and bubble size into the chart series at the specified index. |
| [Remove](../../aspose.words.drawing.charts/chartseries/remove/)(*int*) | Removes the X value, Y value, and bubble size, if supported, from the chart series at the specified index. The corresponding data point and data label are also removed. |

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

* interface [IChartDataPoint](../ichartdatapoint/)
* namespace [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* assembly [Aspose.Words](../../)
