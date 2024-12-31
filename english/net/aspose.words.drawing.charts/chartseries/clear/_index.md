---
title: ChartSeries.Clear
linktitle: Clear
articleTitle: Clear
second_title: Aspose.Words for .NET
description: ChartSeries Clear method. Removes all data values from the chart series. Format of all individual data points and data labels is cleared in C#.
type: docs
weight: 170
url: /net/aspose.words.drawing.charts/chartseries/clear/
---
## ChartSeries.Clear method

Removes all data values from the chart series. Format of all individual data points and data labels is cleared.

```csharp
public void Clear()
```

## Examples

Shows how to populate chart series with data.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);
Chart chart = shape.Chart;
ChartSeries series1 = chart.Series[0];

// Clear X and Y values of the first series.
series1.ClearValues();

// Populate the series with data.
series1.Add(ChartXValue.FromDouble(3), ChartYValue.FromDouble(10), 10);
series1.Add(ChartXValue.FromDouble(5), ChartYValue.FromDouble(5));
series1.Add(ChartXValue.FromDouble(7), ChartYValue.FromDouble(11));
series1.Add(ChartXValue.FromDouble(9));

ChartSeries series2 = chart.Series[1];
// Clear X and Y values of the second series.
series2.Clear();

// Populate the series with data.
series2.Add(ChartXValue.FromDouble(2), ChartYValue.FromDouble(4));
series2.Add(ChartXValue.FromDouble(4), ChartYValue.FromDouble(7));
series2.Add(ChartXValue.FromDouble(6), ChartYValue.FromDouble(14));
series2.Add(ChartXValue.FromDouble(8), ChartYValue.FromDouble(7));

doc.Save(ArtifactsDir + "Charts.PopulateChartWithData.docx");
```

### See Also

* class [ChartSeries](../)
* namespace [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* assembly [Aspose.Words](../../../)
