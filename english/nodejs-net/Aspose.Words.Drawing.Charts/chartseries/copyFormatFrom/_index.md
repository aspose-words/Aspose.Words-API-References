---
title: ChartSeries.copyFormatFrom method
linktitle: copyFormatFrom method
articleTitle: copyFormatFrom method
second_title: Aspose.Words for NodeJs
description: "ChartSeries.copyFormatFrom method. Copies default data point format from the data point with the specified index."
type: docs
weight: 190
url: /nodejs-net/Aspose.Words.Drawing.Charts/chartseries/copyFormatFrom/
---

## copyFormatFrom(dataPointIndex) {#number}

Copies default data point format from the data point with the specified index.


```js
copyFormatFrom(dataPointIndex: number)
```

| Parameter | Type | Description |
| --- | --- | --- |
| dataPointIndex | number |  |

### Examples

Shows how to copy data point format.

```js
let doc = new aw.Document(base.myDir + "DataPoint format.docx");

// Get the chart and series to update format.
let shape = doc.getShape(0, true);
let series = shape.chart.series.at(0);
let dataPoints = series.dataPoints;

expect(dataPoints.hasDefaultFormat(0)).toEqual(true);
expect(dataPoints.hasDefaultFormat(1)).toEqual(false);

// Copy format of the data point with index 1 to the data point with index 2
// so that the data point 2 looks the same as the data point 1.
dataPoints.copyFormat(0, 1);

expect(dataPoints.hasDefaultFormat(0)).toEqual(true);
expect(dataPoints.hasDefaultFormat(1)).toEqual(true);

// Copy format of the data point with index 0 to the series defaults so that all data points
// in the series that have the default format look the same as the data point 0.
series.copyFormatFrom(1);

expect(dataPoints.hasDefaultFormat(0)).toEqual(true);
expect(dataPoints.hasDefaultFormat(1)).toEqual(true);

doc.save(base.artifactsDir + "Charts.CopyDataPointFormat.docx");
```

### See Also

* module [Aspose.Words.Drawing.Charts](../../)
* class [ChartSeries](../)

