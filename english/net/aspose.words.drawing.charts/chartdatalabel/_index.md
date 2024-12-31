---
title: ChartDataLabel Class
linktitle: ChartDataLabel
articleTitle: ChartDataLabel
second_title: Aspose.Words for .NET
description: Aspose.Words.Drawing.Charts.ChartDataLabel class. Represents data label on a chart point or trendline in C#.
type: docs
weight: 920
url: /net/aspose.words.drawing.charts/chartdatalabel/
---
## ChartDataLabel class

Represents data label on a chart point or trendline.

To learn more, visit the [Working with Charts](https://docs.aspose.com/words/net/working-with-charts/) documentation article.

```csharp
public class ChartDataLabel
```

## Properties

| Name | Description |
| --- | --- |
| [Font](../../aspose.words.drawing.charts/chartdatalabel/font/) { get; } | Provides access to the font formatting of this data label. |
| [Format](../../aspose.words.drawing.charts/chartdatalabel/format/) { get; } | Provides access to fill and line formatting of the data label. |
| [Index](../../aspose.words.drawing.charts/chartdatalabel/index/) { get; } | Specifies the index of the containing element. This index shall determine which of the parent's children collection this element applies to. Default value is 0. |
| [IsHidden](../../aspose.words.drawing.charts/chartdatalabel/ishidden/) { get; set; } | Gets/sets a flag indicating whether this label is hidden. The default value is `false`. |
| [IsVisible](../../aspose.words.drawing.charts/chartdatalabel/isvisible/) { get; } | Returns `true` if this data label has something to display. |
| [Left](../../aspose.words.drawing.charts/chartdatalabel/left/) { get; set; } | Gets or sets the distance of the data label in points from the left edge of the chart or from the position specified by its [`Position`](./position/) property, depending on the value of the [`LeftMode`](./leftmode/) property. |
| [LeftMode](../../aspose.words.drawing.charts/chartdatalabel/leftmode/) { get; set; } | Gets or sets the interpretation mode of the [`Left`](./left/) property value: whether it sets the location of the data label from the left edge of the chart of from the position specified by its [`Position`](./position/) property. |
| [NumberFormat](../../aspose.words.drawing.charts/chartdatalabel/numberformat/) { get; } | Returns number format of the parent element. |
| [Orientation](../../aspose.words.drawing.charts/chartdatalabel/orientation/) { get; set; } | Gets or sets the orientation of the label text. |
| [Position](../../aspose.words.drawing.charts/chartdatalabel/position/) { get; set; } | Gets or sets the position of the data label. |
| [Rotation](../../aspose.words.drawing.charts/chartdatalabel/rotation/) { get; set; } | Gets or sets the rotation of the label in degrees. |
| [Separator](../../aspose.words.drawing.charts/chartdatalabel/separator/) { get; set; } | Gets or sets string separator used for the data labels on a chart. The default is a comma, except for pie charts showing only category name and percentage, when a line break shall be used instead. |
| [ShowBubbleSize](../../aspose.words.drawing.charts/chartdatalabel/showbubblesize/) { get; set; } | Allows to specify if bubble size is to be displayed for the data labels on a chart. Applies only to Bubble charts. Default value is `false`. |
| [ShowCategoryName](../../aspose.words.drawing.charts/chartdatalabel/showcategoryname/) { get; set; } | Allows to specify if category name is to be displayed for the data labels on a chart. Default value is `false`. |
| [ShowDataLabelsRange](../../aspose.words.drawing.charts/chartdatalabel/showdatalabelsrange/) { get; set; } | Allows to specify if values from data labels range to be displayed in the data labels. Default value is `false`. |
| [ShowLeaderLines](../../aspose.words.drawing.charts/chartdatalabel/showleaderlines/) { get; set; } | Allows to specify if data label leader lines need be shown. Default value is `false`. |
| [ShowLegendKey](../../aspose.words.drawing.charts/chartdatalabel/showlegendkey/) { get; set; } | Allows to specify if legend key is to be displayed for the data labels on a chart. Default value is `false`. |
| [ShowPercentage](../../aspose.words.drawing.charts/chartdatalabel/showpercentage/) { get; set; } | Allows to specify if percentage value is to be displayed for the data labels on a chart. Default value is `false`. |
| [ShowSeriesName](../../aspose.words.drawing.charts/chartdatalabel/showseriesname/) { get; set; } | Returns or sets a Boolean to indicate the series name display behavior for the data labels on a chart. `true` to show the series name; `false` to hide. By default `false`. |
| [ShowValue](../../aspose.words.drawing.charts/chartdatalabel/showvalue/) { get; set; } | Allows to specify if values are to be displayed in the data labels. Default value is `false`. |
| [Top](../../aspose.words.drawing.charts/chartdatalabel/top/) { get; set; } | Gets or sets the distance of the data label in points from the top edge of the chart or from the position specified by its [`Position`](./position/) property, depending on the value of the [`TopMode`](./topmode/) property. |
| [TopMode](../../aspose.words.drawing.charts/chartdatalabel/topmode/) { get; set; } | Gets or sets the interpretation mode of the [`Top`](./top/) property value: whether it sets the location of the data label from the top edge of the chart of from the position specified by its [`Position`](./position/) property. |

## Methods

| Name | Description |
| --- | --- |
| [ClearFormat](../../aspose.words.drawing.charts/chartdatalabel/clearformat/)() | Clears format of this data label. The properties are set to the default values defined in the parent data label collection. |

## Remarks

On a series, the `ChartDataLabel` object is a member of the [`ChartDataLabelCollection`](../chartdatalabelcollection/). The [`ChartDataLabelCollection`](../chartdatalabelcollection/) contains a `ChartDataLabel` object for each point.

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

    ChartDataLabel dataLabel = chart.Series[1].DataLabels[2];
    dataLabel.Format.Fill.Color = Color.Red;

    // For a cleaner looking graph, we can remove data labels individually.
    dataLabel.ClearFormat();

    // We can also strip an entire series of its data labels at once.
    chart.Series[2].DataLabels.ClearFormat();

    doc.Save(ArtifactsDir + "Charts.DataLabels.docx");
}

/// <summary>
/// Apply data labels with custom number format and separator to several data points in a series.
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

### See Also

* namespace [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* assembly [Aspose.Words](../../)
