---
title: ChartDataLabelCollection.showSeriesName property
linktitle: showSeriesName property
articleTitle: showSeriesName property
second_title: Aspose.Words for NodeJs
description: "ChartDataLabelCollection.showSeriesName property. Returns or sets a Boolean to indicate the series name display behavior for the data labels of the entire series"
type: docs
weight: 150
url: /nodejs-net/Aspose.Words.Drawing.Charts/chartdatalabelcollection/showSeriesName/
---

## ChartDataLabelCollection.showSeriesName property

Returns or sets a Boolean to indicate the series name display behavior for the data labels of the entire series.
``True`` to show the series name; ``False`` to hide. By default ``False``.



```js
get showSeriesName(): boolean
```

### Remarks

Value defined for this property can be overridden for an individual data label with using the
[ChartDataLabel.showSeriesName](../../chartdatalabel/showSeriesName/) property.



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

### See Also

* module [Aspose.Words.Drawing.Charts](../../)
* class [ChartDataLabelCollection](../)

