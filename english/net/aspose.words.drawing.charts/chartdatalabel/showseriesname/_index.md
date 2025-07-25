---
title: ChartDataLabel.ShowSeriesName
linktitle: ShowSeriesName
articleTitle: ShowSeriesName
second_title: Aspose.Words for .NET
description: Discover the ChartDataLabel ShowSeriesName property, easily control series name visibility on your charts. Enhance data clarity with a simple Boolean setting!
type: docs
weight: 190
url: /net/aspose.words.drawing.charts/chartdatalabel/showseriesname/
---
## ChartDataLabel.ShowSeriesName property

Returns or sets a Boolean to indicate the series name display behavior for the data labels on a chart. `true` to show the series name; `false` to hide. By default `false`.

```csharp
public bool ShowSeriesName { get; set; }
```

## Examples

Shows how to apply labels to data points in a line chart.

```csharp
public void DataLabels()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    Shape chartShape = builder.InsertChart(ChartType.Line, 400, 300);
    Chart chart = chartShape.Chart;

    Assert.That(chart.Series.Count, Is.EqualTo(3));
    Assert.That(chart.Series[0].Name, Is.EqualTo("Series 1"));
    Assert.That(chart.Series[1].Name, Is.EqualTo("Series 2"));
    Assert.That(chart.Series[2].Name, Is.EqualTo("Series 3"));

    // Apply data labels to every series in the chart.
    // These labels will appear next to each data point in the graph and display its value.
    foreach (ChartSeries series in chart.Series)
    {
        ApplyDataLabels(series, 4, "000.0", ", ");
        Assert.That(series.DataLabels.Count, Is.EqualTo(4));
    }

    // Change the separator string for every data label in a series.
    using (IEnumerator<ChartDataLabel> enumerator = chart.Series[0].DataLabels.GetEnumerator())
    {
        while (enumerator.MoveNext())
        {
            Assert.That(enumerator.Current.Separator, Is.EqualTo(", "));
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
        Assert.That(series.DataLabels[i].IsVisible, Is.False);

        series.DataLabels[i].ShowCategoryName = true;
        series.DataLabels[i].ShowSeriesName = true;
        series.DataLabels[i].ShowValue = true;
        series.DataLabels[i].ShowLeaderLines = true;
        series.DataLabels[i].ShowLegendKey = true;
        series.DataLabels[i].ShowPercentage = false;
        Assert.That(series.DataLabels[i].IsHidden, Is.False);
        Assert.That(series.DataLabels[i].ShowDataLabelsRange, Is.False);

        series.DataLabels[i].NumberFormat.FormatCode = numberFormat;
        series.DataLabels[i].Separator = separator;

        Assert.That(series.DataLabels[i].ShowDataLabelsRange, Is.False);
        Assert.That(series.DataLabels[i].IsVisible, Is.True);
        Assert.That(series.DataLabels[i].IsHidden, Is.False);
    }
}
```

### See Also

* class [ChartDataLabel](../)
* namespace [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* assembly [Aspose.Words](../../../)
