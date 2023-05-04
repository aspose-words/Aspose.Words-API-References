---
title: AxisBound.IsAuto
linktitle: IsAuto
articleTitle: IsAuto
second_title: Aspose.Words for .NET
description: AxisBound IsAuto property. Returns a flag indicating that axis bound should be determined automatically in C#.
type: docs
weight: 20
url: /net/aspose.words.drawing.charts/axisbound/isauto/
---
## AxisBound.IsAuto property

Returns a flag indicating that axis bound should be determined automatically.

```csharp
public bool IsAuto { get; }
```

## Examples

Shows how to set custom axis bounds.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape chartShape = builder.InsertChart(ChartType.Scatter, 450, 300);
Chart chart = chartShape.Chart;

// Clear the chart's demo data series to start with a clean chart.
chart.Series.Clear();

// Add a series with two decimal arrays. The first array contains the X-values,
// and the second contains corresponding Y-values for points in the scatter chart.
chart.Series.Add("Series 1", 
    new[] { 1.1, 5.4, 7.9, 3.5, 2.1, 9.7 }, 
    new[] { 2.1, 0.3, 0.6, 3.3, 1.4, 1.9 });

// By default, default scaling is applied to the graph's X and Y-axes,
// so that both their ranges are big enough to encompass every X and Y-value of every series.
Assert.True(chart.AxisX.Scaling.Minimum.IsAuto);

// We can define our own axis bounds.
// In this case, we will make both the X and Y-axis rulers show a range of 0 to 10.
chart.AxisX.Scaling.Minimum = new AxisBound(0);
chart.AxisX.Scaling.Maximum = new AxisBound(10);
chart.AxisY.Scaling.Minimum = new AxisBound(0);
chart.AxisY.Scaling.Maximum = new AxisBound(10);

Assert.False(chart.AxisX.Scaling.Minimum.IsAuto);
Assert.False(chart.AxisY.Scaling.Minimum.IsAuto);

// Create a line chart with a series requiring a range of dates on the X-axis, and decimal values for the Y-axis.
chartShape = builder.InsertChart(ChartType.Line, 450, 300);
chart = chartShape.Chart;
chart.Series.Clear();

DateTime[] dates = { new DateTime(1973, 5, 11),
    new DateTime(1981, 2, 4),
    new DateTime(1985, 9, 23),
    new DateTime(1989, 6, 28),
    new DateTime(1994, 12, 15)
};

chart.Series.Add("Series 1", dates, new[] { 3.0, 4.7, 5.9, 7.1, 8.9 });

// We can set axis bounds in the form of dates as well, limiting the chart to a period.
// Setting the range to 1980-1990 will omit the two of the series values
// that are outside of the range from the graph.
chart.AxisX.Scaling.Minimum = new AxisBound(new DateTime(1980, 1, 1));
chart.AxisX.Scaling.Maximum = new AxisBound(new DateTime(1990, 1, 1));

doc.Save(ArtifactsDir + "Charts.AxisBound.docx");
```

### See Also

* class [AxisBound](../)
* namespace [Aspose.Words.Drawing.Charts](../../axisbound/)
* assembly [Aspose.Words](../../../)
