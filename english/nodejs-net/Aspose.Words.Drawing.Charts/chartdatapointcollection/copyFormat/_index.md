---
title: ChartDataPointCollection.copyFormat method
linktitle: copyFormat method
articleTitle: copyFormat method
second_title: Aspose.Words for NodeJs
description: "ChartDataPointCollection.copyFormat method. Copies format from the source data point to the destination data point."
type: docs
weight: 40
url: /nodejs-net/Aspose.Words.Drawing.Charts/chartdatapointcollection/copyFormat/
---

## copyFormat(sourceIndex, destinationIndex) {#number_number}

Copies format from the source data point to the destination data point.


```js
copyFormat(sourceIndex: numberdestinationIndex: number)
```

| Parameter | Type | Description |
| --- | --- | --- |
| sourceIndex | number |  |
| destinationIndex | number |  |

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
* class [ChartDataPointCollection](../)

