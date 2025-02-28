---
title: ChartDataLabelCollection.ShowSeriesName
linktitle: ShowSeriesName
articleTitle: ShowSeriesName
second_title: Aspose.Words for .NET
description: Discover the ChartDataLabelCollection ShowSeriesName property: easily control series name visibility in your data labels. Enhance your charts today!
type: docs
weight: 160
url: /net/aspose.words.drawing.charts/chartdatalabelcollection/showseriesname/
---
## ChartDataLabelCollection.ShowSeriesName property

Returns or sets a Boolean to indicate the series name display behavior for the data labels of the entire series. `true` to show the series name; `false` to hide. By default `false`.

```csharp
public bool ShowSeriesName { get; set; }
```

## Remarks

Value defined for this property can be overridden for an individual data label with using the [`ShowSeriesName`](../../chartdatalabel/showseriesname/) property.

## Examples

Shows how to work with data labels of a bubble chart.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Chart chart = builder.InsertChart(ChartType.Bubble, 500, 300).Chart;

// Clear the chart's demo data series to start with a clean chart.
chart.Series.Clear();

// Add a custom series with X/Y coordinates and diameter of each of the bubbles. 
ChartSeries series = chart.Series.Add("Aspose Test Series",
    new[] { 2.9, 3.5, 1.1, 4.0, 4.0 },
    new[] { 1.9, 8.5, 2.1, 6.0, 1.5 },
    new[] { 9.0, 4.5, 2.5, 8.0, 5.0 });

// Enable data labels, and then modify their appearance.
series.HasDataLabels = true;
ChartDataLabelCollection dataLabels = series.DataLabels;
dataLabels.ShowBubbleSize = true;
dataLabels.ShowCategoryName = true;
dataLabels.ShowSeriesName = true;
dataLabels.Separator = " & ";

doc.Save(ArtifactsDir + "Charts.DataLabelsBubbleChart.docx");
```

### See Also

* class [ChartDataLabelCollection](../)
* namespace [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* assembly [Aspose.Words](../../../)
