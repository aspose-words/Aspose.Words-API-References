---
title: ChartDataLabel
second_title: Aspose.Words for .NET API Reference
description: 
type: docs
weight: 620
url: /net/aspose.words.drawing.charts/chartdatalabel/
---
## ChartDataLabel class

Represents data label on a chart point or trendline.

```csharp
public class ChartDataLabel
```

## Properties

| Name | Description |
| --- | --- |
| [Index](index) { get; } | Specifies the index of the containing element. This index shall determine which of the parent's children collection this element applies to. Default value is 0. |
| [IsHidden](ishidden) { get; set; } | Gets/sets a flag indicating whether this label is hidden. The default value is **false**. |
| [IsVisible](isvisible) { get; } | Returns true if this data label has something to display. |
| [NumberFormat](numberformat) { get; } | Returns number format of the parent element. |
| [Separator](separator) { get; set; } | Gets or sets string separator used for the data labels on a chart. The default is a comma, except for pie charts showing only category name and percentage, when a line break shall be used instead. |
| [ShowBubbleSize](showbubblesize) { get; set; } | Allows to specify if bubble size is to be displayed for the data labels on a chart. Applies only to Bubble charts. Default value is false. |
| [ShowCategoryName](showcategoryname) { get; set; } | Allows to specify if category name is to be displayed for the data labels on a chart. Default value is false. |
| [ShowDataLabelsRange](showdatalabelsrange) { get; set; } | Allows to specify if values from data labels range to be displayed in the data labels. Default value is false. |
| [ShowLeaderLines](showleaderlines) { get; set; } | Allows to specify if data label leader lines need be shown. Default value is false. |
| [ShowLegendKey](showlegendkey) { get; set; } | Allows to specify if legend key is to be displayed for the data labels on a chart. Default value is false. |
| [ShowPercentage](showpercentage) { get; set; } | Allows to specify if percentage value is to be displayed for the data labels on a chart. Default value is false. |
| [ShowSeriesName](showseriesname) { get; set; } | Returns or sets a Boolean to indicate the series name display behavior for the data labels on a chart. True to show the series name. False to hide. By default false. |
| [ShowValue](showvalue) { get; set; } | Allows to specify if values are to be displayed in the data labels. Default value is false. |

## Methods

| Name | Description |
| --- | --- |
| [ClearFormat](clearformat)() | Clears format of this data label. The properties are set to the default values defined in the parent data label collection. |

### Remarks

On a series, the [`ChartDataLabel`](../chartdatalabel) object is a member of the [`ChartDataLabelCollection`](../chartdatalabelcollection). The [`ChartDataLabelCollection`](../chartdatalabelcollection) contains a [`ChartDataLabel`](../chartdatalabel) object for each point.

### Examples

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

* namespace [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts)
* assembly [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
