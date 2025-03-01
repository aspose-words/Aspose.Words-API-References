---
title: ChartSeries.ClearValues
linktitle: ClearValues
articleTitle: ClearValues
second_title: Aspose.Words for .NET
description: Discover ChartSeries ClearValues, Effortlessly remove data values while preserving your chart's formatting and labels for a cleaner, more professional look.
type: docs
weight: 180
url: /net/aspose.words.drawing.charts/chartseries/clearvalues/
---
## ChartSeries.ClearValues method

Removes all data values from the chart series with preserving the format of the data points and data labels.

```csharp
public void ClearValues()
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
