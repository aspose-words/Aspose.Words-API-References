---
title: ChartSeries.IsTotal
linktitle: IsTotal
articleTitle: IsTotal
second_title: Aspose.Words for .NET
description: ChartSeries IsTotal method. Determines whether the data point at the specified index is a total. Applies only to Waterfall charts.
type: docs
weight: 210
url: /net/aspose.words.drawing.charts/chartseries/istotal/
---
## ChartSeries.IsTotal method

Determines whether the data point at the specified index is a total. Applies only to Waterfall charts.

```csharp
public bool IsTotal(int index)
```

| Parameter | Type | Description |
| --- | --- | --- |
| index | Int32 | The zero-based index of the data point. |

### Return Value

**true** if the data point is a total; otherwise, **false**.

## Examples

Shows how to determine whether a data point is a total in a waterfall chart.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insert a Waterfall chart.
Shape shape = builder.InsertChart(ChartType.Waterfall, 450, 450);
Chart chart = shape.Chart;
chart.Title.Text = "New Zealand GDP";

// Delete default generated series.
chart.Series.Clear();

// Add a series where the start value, the subtotal and the final value are totals.
ChartSeries series = chart.Series.Add(
    "New Zealand GDP",
    new string[] { "2018", "2019 growth", "2020 growth", "2020", "2021 growth", "2022 growth", "2022" },
    new double[] { 100, 0.57, -0.25, 100.32, 20.22, -2.92, 117.62 },
    new bool[] { true, false, false, true, false, false, true });

// Print the type of each data point.
for (int i = 0; i < series.YValues.Count; i++)
{
    if (series.IsTotal(i))
        Console.WriteLine($"Data point {i} is Subtotal");
    else if (series.YValues[i].DoubleValue > 0)
        Console.WriteLine($"Data point {i} is Increase");
    else
        Console.WriteLine($"Data point {i} is Decrease");
}

// The same flag is available on the data point itself.
Console.WriteLine($"Data point 3 is total: {series.DataPoints[3].IsTotal}");

doc.Save(ArtifactsDir + "Charts.ChartSeriesAndDataPointIsTotal.docx");
```

### See Also

* class [ChartSeries](../)
* namespace [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* assembly [Aspose.Words](../../../)
