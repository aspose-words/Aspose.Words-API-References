---
title: ChartDataLabelCollection.ShowValue
linktitle: ShowValue
articleTitle: ShowValue
second_title: Aspose.Words for .NET
description: Discover how the ShowValue property in ChartDataLabelCollection enhances your data visualization by displaying series values. Optimize your charts today!
type: docs
weight: 170
url: /net/aspose.words.drawing.charts/chartdatalabelcollection/showvalue/
---
## ChartDataLabelCollection.ShowValue property

Allows to specify whether values are to be displayed in the data labels of the entire series. Default value is `false`.

```csharp
public bool ShowValue { get; set; }
```

## Remarks

Value defined for this property can be overridden for an individual data label with using the [`ShowValue`](../../chartdatalabel/showvalue/) property.

## Examples

Shows how to work with data labels of a pie chart.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Chart chart = builder.InsertChart(ChartType.Pie, 500, 300).Chart;

// Clear the chart's demo data series to start with a clean chart.
chart.Series.Clear();

// Insert a custom chart series with a category name for each of the sectors, and their frequency table.
ChartSeries series = chart.Series.Add("Aspose Test Series",
    new[] { "Word", "PDF", "Excel" },
    new[] { 2.7, 3.2, 0.8 });

// Enable data labels that will display both percentage and frequency of each sector, and modify their appearance.
series.HasDataLabels = true;
ChartDataLabelCollection dataLabels = series.DataLabels;
dataLabels.ShowLeaderLines = true;
dataLabels.ShowLegendKey = true;
dataLabels.ShowPercentage = true;
dataLabels.ShowValue = true;
dataLabels.Separator = "; ";

doc.Save(ArtifactsDir + "Charts.DataLabelsPieChart.docx");
```

### See Also

* class [ChartDataLabelCollection](../)
* namespace [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* assembly [Aspose.Words](../../../)
