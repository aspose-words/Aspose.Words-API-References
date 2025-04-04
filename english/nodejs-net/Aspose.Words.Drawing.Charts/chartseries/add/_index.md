---
title: ChartSeries.add method
linktitle: add method
articleTitle: add method
second_title: Aspose.Words for Node.js
description: "Aspose.Words.Drawing.Charts.ChartSeries.add method"
type: docs
weight: 160
url: /nodejs-net/aspose.words.drawing.charts/chartseries/add/
---

## add(xValue) {#chartxvalue}

Adds the specified X value to the chart series. If the series supports Y values and bubble sizes, they will
be empty for the X value.


```js
add(xValue: Aspose.Words.Drawing.Charts.ChartXValue)
```

| Parameter | Type | Description |
| --- | --- | --- |
| xValue | [ChartXValue](../../chartxvalue/) |  |

## add(xValue, yValue) {#chartxvalue_chartyvalue}

Adds the specified X and Y values to the chart series.


```js
add(xValue: Aspose.Words.Drawing.Charts.ChartXValue, yValue: Aspose.Words.Drawing.Charts.ChartYValue)
```

| Parameter | Type | Description |
| --- | --- | --- |
| xValue | [ChartXValue](../../chartxvalue/) |  |
| yValue | [ChartYValue](../../chartyvalue/) |  |

## add(xValue, yValue, bubbleSize) {#chartxvalue_chartyvalue_number}

Adds the specified X value, Y value and bubble size to the chart series.


```js
add(xValue: Aspose.Words.Drawing.Charts.ChartXValue, yValue: Aspose.Words.Drawing.Charts.ChartYValue, bubbleSize: number)
```

| Parameter | Type | Description |
| --- | --- | --- |
| xValue | [ChartXValue](../../chartxvalue/) |  |
| yValue | [ChartYValue](../../chartyvalue/) |  |
| bubbleSize | number |  |

## Examples

Shows how to populate chart series with data.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder();

let shape = builder.insertChart(aw.Drawing.Charts.ChartType.Column, 432, 252);
let chart = shape.chart;
let series1 = chart.series.at(0);

// Clear X and Y values of the first series.
series1.clearValues();

// Populate the series with data.
series1.add(aw.Drawing.Charts.ChartXValue.fromDouble(3), aw.Drawing.Charts.ChartYValue.fromDouble(10));
series1.add(aw.Drawing.Charts.ChartXValue.fromDouble(5), aw.Drawing.Charts.ChartYValue.fromDouble(5));
series1.add(aw.Drawing.Charts.ChartXValue.fromDouble(7), aw.Drawing.Charts.ChartYValue.fromDouble(11));
series1.add(aw.Drawing.Charts.ChartXValue.fromDouble(9), aw.Drawing.Charts.ChartYValue.fromDouble(17));

let series2 = chart.series.at(1);

// Clear X and Y values of the second series.
series2.clearValues();

// Populate the series with data.
series2.add(aw.Drawing.Charts.ChartXValue.fromDouble(2), aw.Drawing.Charts.ChartYValue.fromDouble(4));
series2.add(aw.Drawing.Charts.ChartXValue.fromDouble(4), aw.Drawing.Charts.ChartYValue.fromDouble(7));
series2.add(aw.Drawing.Charts.ChartXValue.fromDouble(6), aw.Drawing.Charts.ChartYValue.fromDouble(14));
series2.add(aw.Drawing.Charts.ChartXValue.fromDouble(8), aw.Drawing.Charts.ChartYValue.fromDouble(7));

doc.save(base.artifactsDir + "Charts.PopulateChartWithData.docx");
```

Shows how to add/remove chart data values.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder();

let shape = builder.insertChart(aw.Drawing.Charts.ChartType.Column, 432, 252);
let chart = shape.chart;
let department1Series = chart.series.at(0);
let department2Series = chart.series.at(1);

// Remove the first value in the both series.
department1Series.remove(0);
department2Series.remove(0);

// Add new values to the both series.
let newXCategory = aw.Drawing.Charts.ChartXValue.fromString("Q1, 2023");
department1Series.add(newXCategory, aw.Drawing.Charts.ChartYValue.fromDouble(10.3));
department2Series.add(newXCategory, aw.Drawing.Charts.ChartYValue.fromDouble(5.7));

doc.save(base.artifactsDir + "Charts.ChartDataValues.docx");
```

## See Also

* module [Aspose.Words.Drawing.Charts](../../)
* class [ChartSeries](../)

