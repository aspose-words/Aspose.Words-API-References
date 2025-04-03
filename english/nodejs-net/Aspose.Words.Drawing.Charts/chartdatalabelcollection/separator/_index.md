---
title: ChartDataLabelCollection.separator property
linktitle: separator property
articleTitle: separator property
second_title: Aspose.Words for NodeJs
description: "ChartDataLabelCollection.separator property. Gets or sets string separator used for the data labels of the entire series"
type: docs
weight: 80
url: /nodejs-net/aspose.words.drawing.charts/chartdatalabelcollection/separator/
---

## ChartDataLabelCollection.separator property

Gets or sets string separator used for the data labels of the entire series. 
The default is a comma, except for pie charts showing only category name and percentage, when a line break 
shall be used instead.


```js
get separator(): string
```

### Remarks

Value defined for this property can be overridden for an individual data label with using the
[ChartDataLabel.separator](../../chartdatalabel/separator/) property.



### Examples

Shows how to work with data labels of a bubble chart.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

let chart = builder.insertChart(aw.Drawing.Charts.ChartType.Bubble, 500, 300).chart;

// Clear the chart's demo data series to start with a clean chart.
chart.series.clear();

// Add a custom series with X/Y coordinates and diameter of each of the bubbles. 
let series = chart.series.add("Aspose Test Series",
  [ 2.9, 3.5, 1.1, 4.0, 4.0 ],
  [ 1.9, 8.5, 2.1, 6.0, 1.5 ],
  [ 9.0, 4.5, 2.5, 8.0, 5.0 ]);

// Enable data labels, and then modify their appearance.
series.hasDataLabels = true;
let dataLabels = series.dataLabels;
dataLabels.showBubbleSize = true;
dataLabels.showCategoryName = true;
dataLabels.showSeriesName = true;
dataLabels.separator = " & ";

doc.save(base.artifactsDir + "Charts.DataLabelsBubbleChart.docx");
```

Shows how to work with data labels of a pie chart.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

let chart = builder.insertChart(aw.Drawing.Charts.ChartType.Pie, 500, 300).chart;

// Clear the chart's demo data series to start with a clean chart.
chart.series.clear();

// Insert a custom chart series with a category name for each of the sectors, and their frequency table.
let series = chart.series.add("Aspose Test Series",
  [ "Word", "PDF", "Excel" ],
  [ 2.7, 3.2, 0.8 ]);

// Enable data labels that will display both percentage and frequency of each sector, and modify their appearance.
series.hasDataLabels = true;
let dataLabels = series.dataLabels;
dataLabels.showLeaderLines = true;
dataLabels.showLegendKey = true;
dataLabels.showPercentage = true;
dataLabels.showValue = true;
dataLabels.separator = "; ";

doc.save(base.artifactsDir + "Charts.DataLabelsPieChart.docx");
```

### See Also

* module [Aspose.Words.Drawing.Charts](../../)
* class [ChartDataLabelCollection](../)

