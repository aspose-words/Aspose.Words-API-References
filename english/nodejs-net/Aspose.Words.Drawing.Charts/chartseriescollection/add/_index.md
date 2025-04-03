---
title: ChartSeriesCollection.add method
linktitle: add method
articleTitle: add method
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.Drawing.Charts.ChartSeriesCollection.add method"
type: docs
weight: 30
url: /nodejs-net/aspose.words.drawing.charts/chartseriescollection/add/
---

## add(seriesName, categories, values) {#string_string[]_number[]}

Adds new [ChartSeries](../../chartseries/) to this collection.
Use this method to add series to any type of Bar, Column, Line and Surface charts.



```js
add(seriesName: stringcategories: string[]values: number[])
```

| Parameter | Type | Description |
| --- | --- | --- |
| seriesName | string |  |
| categories | string[] |  |
| values | number[] |  |

### Returns

Recently added [ChartSeries](../../chartseries/) object.


## add(seriesName, xValues, yValues) {#string_number[]_number[]}

Adds new [ChartSeries](../../chartseries/) to this collection.
Use this method to add series to any type of Scatter charts.



```js
add(seriesName: stringxValues: number[]yValues: number[])
```

| Parameter | Type | Description |
| --- | --- | --- |
| seriesName | string |  |
| xValues | number[] |  |
| yValues | number[] |  |

### Returns

Recently added [ChartSeries](../../chartseries/) object.


## add(seriesName, dates, values) {#string_date[]_number[]}

Adds new [ChartSeries](../../chartseries/) to this collection.
Use this method to add series to any type of Area, Radar and Stock charts.



```js
add(seriesName: stringdates: Date[]values: number[])
```

| Parameter | Type | Description |
| --- | --- | --- |
| seriesName | string |  |
| dates | Date[] |  |
| values | number[] |  |

## add(seriesName, xValues, yValues, bubbleSizes) {#string_number[]_number[]_number[]}

Adds new [ChartSeries](../../chartseries/) to this collection.
Use this method to add series to any type of Bubble charts.



```js
add(seriesName: stringxValues: number[]yValues: number[]bubbleSizes: number[])
```

| Parameter | Type | Description |
| --- | --- | --- |
| seriesName | string |  |
| xValues | number[] |  |
| yValues | number[] |  |
| bubbleSizes | number[] |  |

### Returns

Recently added [ChartSeries](../../chartseries/) object.


## add(seriesName, categories, values) {#string_chartmultilevelvalue[]_number[]}

Adds new [ChartSeries](../../chartseries/) to this collection.
Use this method to add series that have multi-level data categories.



```js
add(seriesName: stringcategories: Aspose.Words.Drawing.Charts.ChartMultilevelValue[]values: number[])
```

| Parameter | Type | Description |
| --- | --- | --- |
| seriesName | string |  |
| categories | [ChartMultilevelValue](../../chartmultilevelvalue/)[] |  |
| values | number[] |  |

### Returns

Recently added [ChartSeries](../../chartseries/) object.


## add(seriesName, xValues) {#string_number[]}

Adds new [ChartSeries](../../chartseries/) to this collection.
Use this method to add series to Histogram charts.



```js
add(seriesName: stringxValues: number[])
```

| Parameter | Type | Description |
| --- | --- | --- |
| seriesName | string |  |
| xValues | number[] |  |

### Remarks

For chart types other than Histogram, this method adds a series with empty Y values.


### Returns

Recently added [ChartSeries](../../chartseries/) object.


## add(seriesName, categories, values, isSubtotal) {#string_string[]_number[]_boolean[]}

Adds new [ChartSeries](../../chartseries/) to this collection.
Use this method to add series to Waterfall charts.



```js
add(seriesName: stringcategories: string[]values: number[]isSubtotal: boolean[])
```

| Parameter | Type | Description |
| --- | --- | --- |
| seriesName | string | A name of the series to be added. |
| categories | string[] | Category names for the X axis. |
| values | number[] | Y-axis values. |
| isSubtotal | boolean[] | Values indicating whether the corresponding Y value is a subtotal. |

### Remarks

For chart types other than Waterfall, *isSubtotal* values are ignored.


### Returns

Recently added [ChartSeries](../../chartseries/) object.


## See Also

* module [Aspose.Words.Drawing.Charts](../../)
* class [ChartSeriesCollection](../)

