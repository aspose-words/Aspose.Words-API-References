---
title: ChartSeries.insert method
linktitle: insert method
articleTitle: insert method
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.Drawing.Charts.ChartSeries.insert method"
type: docs
weight: 200
url: /nodejs-net/aspose.words.drawing.charts/chartseries/insert/
---

## insert(index, xValue) {#number_chartxvalue}

Inserts the specified X value into the chart series at the specified index. If the series supports Y values
and bubble sizes, they will be empty for the X value.


```js
insert(index: number, xValue: Aspose.Words.Drawing.Charts.ChartXValue)
```

| Parameter | Type | Description |
| --- | --- | --- |
| index | number |  |
| xValue | [ChartXValue](../../chartxvalue/) |  |

### Remarks

The corresponding data point with default formatting will be inserted into the data point collection. And,
if data labels are displayed, the corresponding data label with default formatting will be inserted too.


## insert(index, xValue, yValue) {#number_chartxvalue_chartyvalue}

Inserts the specified X and Y values into the chart series at the specified index.


```js
insert(index: number, xValue: Aspose.Words.Drawing.Charts.ChartXValue, yValue: Aspose.Words.Drawing.Charts.ChartYValue)
```

| Parameter | Type | Description |
| --- | --- | --- |
| index | number |  |
| xValue | [ChartXValue](../../chartxvalue/) |  |
| yValue | [ChartYValue](../../chartyvalue/) |  |

### Remarks

The corresponding data point with default formatting will be inserted into the data point collection. And,
if data labels are displayed, the corresponding data label with default formatting will be inserted too.


## insert(index, xValue, yValue, bubbleSize) {#number_chartxvalue_chartyvalue_number}

Inserts the specified X value, Y value and bubble size into the chart series at the specified index.


```js
insert(index: number, xValue: Aspose.Words.Drawing.Charts.ChartXValue, yValue: Aspose.Words.Drawing.Charts.ChartYValue, bubbleSize: number)
```

| Parameter | Type | Description |
| --- | --- | --- |
| index | number |  |
| xValue | [ChartXValue](../../chartxvalue/) |  |
| yValue | [ChartYValue](../../chartyvalue/) |  |
| bubbleSize | number |  |

### Remarks

The corresponding data point with default formatting will be inserted into the data point collection. And,
if data labels are displayed, the corresponding data label with default formatting will be inserted too.


## See Also

* module [Aspose.Words.Drawing.Charts](../../)
* class [ChartSeries](../)

