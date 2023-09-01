---
title: MarkerSymbol Enum
linktitle: MarkerSymbol
articleTitle: MarkerSymbol
second_title: Aspose.Words for .NET
description: Aspose.Words.Drawing.Charts.MarkerSymbol enum. Specifies marker symbol style in C#.
type: docs
weight: 920
url: /net/aspose.words.drawing.charts/markersymbol/
---
## MarkerSymbol enumeration

Specifies marker symbol style.

```csharp
public enum MarkerSymbol
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Default | `0` | Specifies a default marker symbol shall be drawn at each data point. |
| Circle | `1` | Specifies a circle shall be drawn at each data point. |
| Dash | `2` | Specifies a dash shall be drawn at each data point. |
| Diamond | `3` | Specifies a diamond shall be drawn at each data point. |
| Dot | `4` | Specifies a dot shall be drawn at each data point. |
| None | `5` | Specifies nothing shall be drawn at each data point. |
| Picture | `6` | Specifies a picture shall be drawn at each data point. |
| Plus | `7` | Specifies a plus shall be drawn at each data point. |
| Square | `8` | Specifies a square shall be drawn at each data point. |
| Star | `9` | Specifies a star shall be drawn at each data point. |
| Triangle | `10` | Specifies a triangle shall be drawn at each data point. |
| X | `11` | Specifies an X shall be drawn at each data point. |

## Examples

Shows how to work with data points on a line chart.

```csharp
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

* namespace [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* assembly [Aspose.Words](../../)
