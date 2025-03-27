---
title: ChartDataPointCollection.hasDefaultFormat method
linktitle: hasDefaultFormat method
articleTitle: hasDefaultFormat method
second_title: Aspose.Words for NodeJs
description: "ChartDataPointCollection.hasDefaultFormat method. Gets a flag indicating whether the data point at the specified index has default format."
type: docs
weight: 50
url: /nodejs-net/Aspose.Words.Drawing.Charts/chartdatapointcollection/hasDefaultFormat/
---

## hasDefaultFormat(dataPointIndex) {#number}

Gets a flag indicating whether the data point at the specified index has default format.


```js
hasDefaultFormat(dataPointIndex: number)
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
* class [ChartDataPointCollection](../)

