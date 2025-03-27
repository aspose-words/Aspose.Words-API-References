---
title: ChartXValue.fromString method
linktitle: fromString method
articleTitle: fromString method
second_title: Aspose.Words for NodeJs
description: "ChartXValue.fromString method. Creates a [ChartXValue](../) instance of the [ChartXValueType.String](../../chartxvaluetype/#String) type."
type: docs
weight: 100
url: /nodejs-net/Aspose.Words.Drawing.Charts/chartxvalue/fromString/
---

## fromString(value) {#string}

Creates a [ChartXValue](../) instance of the [ChartXValueType.String](../../chartxvaluetype/#String) type.



```js
fromString(value: string)
```

| Parameter | Type | Description |
| --- | --- | --- |
| value | string |  |

### Examples

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

### See Also

* module [Aspose.Words.Drawing.Charts](../../)
* class [ChartXValue](../)

