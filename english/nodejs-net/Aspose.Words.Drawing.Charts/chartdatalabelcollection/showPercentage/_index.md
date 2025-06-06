﻿---
title: ChartDataLabelCollection.showPercentage property
linktitle: showPercentage property
articleTitle: showPercentage property
second_title: Aspose.Words for Node.js
description: "ChartDataLabelCollection.showPercentage property. Allows to specify whether percentage value is to be displayed for the data labels of the entire series"
type: docs
weight: 140
url: /nodejs-net/aspose.words.drawing.charts/chartdatalabelcollection/showPercentage/
---

## ChartDataLabelCollection.showPercentage property

Allows to specify whether percentage value is to be displayed for the data labels of the entire series.
Default value is ``false``. Applies only to Pie charts.



```js
get showPercentage(): boolean
```

### Remarks

Value defined for this property can be overridden for an individual data label with using the
[ChartDataLabel.showPercentage](../../chartdatalabel/showPercentage/) property.



### Examples

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

