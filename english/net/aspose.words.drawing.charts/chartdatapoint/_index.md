---
title: Class ChartDataPoint
second_title: Aspose.Words for .NET API Reference
description: Aspose.Words.Drawing.Charts.ChartDataPoint class. Allows to specify formatting of a single data point on the chart in C#.
type: docs
weight: 650
url: /net/aspose.words.drawing.charts/chartdatapoint/
---
## ChartDataPoint class

Allows to specify formatting of a single data point on the chart.

To learn more, visit the [Working with Charts](https://docs.aspose.com/words/net/working-with-charts/) documentation article.

```csharp
public class ChartDataPoint : IChartDataPoint
```

## Properties

| Name | Description |
| --- | --- |
| [Bubble3D](../../aspose.words.drawing.charts/chartdatapoint/bubble3d/) { get; set; } | Specifies whether the bubbles in Bubble chart should have a 3-D effect applied to them. |
| [Explosion](../../aspose.words.drawing.charts/chartdatapoint/explosion/) { get; set; } | Specifies the amount the data point shall be moved from the center of the pie. Can be negative, negative means that property is not set and no explosion should be applied. Applies only to Pie charts. |
| [Format](../../aspose.words.drawing.charts/chartdatapoint/format/) { get; } | Provides access to fill and line formatting of this data point. |
| [Index](../../aspose.words.drawing.charts/chartdatapoint/index/) { get; } | Index of the data point this object applies formatting to. |
| [InvertIfNegative](../../aspose.words.drawing.charts/chartdatapoint/invertifnegative/) { get; set; } | Specifies whether the parent element shall inverts its colors if the value is negative. |
| [Marker](../../aspose.words.drawing.charts/chartdatapoint/marker/) { get; } | Specifies chart data marker. |

## Methods

| Name | Description |
| --- | --- |
| [ClearFormat](../../aspose.words.drawing.charts/chartdatapoint/clearformat/)() | Clears format of this data point. The properties are set to the default values defined in the parent series. |

## Remarks

On a series, the `ChartDataPoint` object is a member of the [`ChartDataPointCollection`](../chartdatapointcollection/). The [`ChartDataPointCollection`](../chartdatapointcollection/) contains a `ChartDataPoint` object for each point.

## Examples

Shows how to work with data points on a line chart.

```csharp
[Test]
public void ChartDataPoint()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    Shape shape = builder.InsertChart(ChartType.Line, 500, 350);
    Chart chart = shape.Chart;

    Assert.AreEqual(3, chart.Series.Count);
    Assert.AreEqual("Series 1", chart.Series[0].Name);
    Assert.AreEqual("Series 2", chart.Series[1].Name);
    Assert.AreEqual("Series 3", chart.Series[2].Name);

    // Emphasize the chart's data points by making them appear as diamond shapes.
    foreach (ChartSeries series in chart.Series) 
        ApplyDataPoints(series, 4, MarkerSymbol.Diamond, 15);

    // Smooth out the line that represents the first data series.
    chart.Series[0].Smooth = true;

    // Verify that data points for the first series will not invert their colors if the value is negative.
    using (IEnumerator<ChartDataPoint> enumerator = chart.Series[0].DataPoints.GetEnumerator())
    {
        while (enumerator.MoveNext())
        {
            Assert.False(enumerator.Current.InvertIfNegative);
        }
    }

    // For a cleaner looking graph, we can clear format individually.
    chart.Series[1].DataPoints[2].ClearFormat();

    // We can also strip an entire series of data points at once.
    chart.Series[2].DataPoints.ClearFormat();

    doc.Save(ArtifactsDir + "Charts.ChartDataPoint.docx");
}

/// <summary>
/// Applies a number of data points to a series.
/// </summary>
private static void ApplyDataPoints(ChartSeries series, int dataPointsCount, MarkerSymbol markerSymbol, int dataPointSize)
{
    for (int i = 0; i < dataPointsCount; i++)
    {
        ChartDataPoint point = series.DataPoints[i];
        point.Marker.Symbol = markerSymbol;
        point.Marker.Size = dataPointSize;

        Assert.AreEqual(i, point.Index);
    }
}
```

### See Also

* interface [IChartDataPoint](../ichartdatapoint/)
* namespace [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* assembly [Aspose.Words](../../)
