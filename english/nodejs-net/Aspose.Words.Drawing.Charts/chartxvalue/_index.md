---
title: ChartXValue class
linktitle: ChartXValue class
articleTitle: ChartXValue class
second_title: Aspose.Words for Node.js
description: "Aspose.Words.Drawing.Charts.ChartXValue class. Represents an X value for a chart series."
type: docs
weight: 410
url: /nodejs-net/aspose.words.drawing.charts/chartxvalue/
---

## ChartXValue class

Represents an X value for a chart series.


### Remarks

This class contains a number of static methods for creating an X value of a particular type. The
[ChartXValue.valueType](./valueType/) property allows you to determine the type of an existing X value.

All non-null X values of a chart series must be of the same [ChartXValueType](../chartxvaluetype/) type.




### Properties

| Name | Description |
| --- | --- |
| [dateTimeValue](./dateTimeValue/) | Gets the stored datetime value. |
| [doubleValue](./doubleValue/) | Gets the stored numeric value. |
| [multilevelValue](./multilevelValue/) | Gets the stored multilevel value. |
| [stringValue](./stringValue/) | Gets the stored string value. |
| [timeValue](./timeValue/) | Gets the stored time value. |
| [valueType](./valueType/) | Gets the type of the X value stored in the object. |

### Methods

| Name | Description |
| --- | --- |
|[ fromDateTime(value)](./fromDateTime/#date) | Creates a [ChartXValue](./) instance of the [ChartXValueType.DateTime](../chartxvaluetype/#DateTime) type. |
|[ fromDouble(value)](./fromDouble/#number) | Creates a [ChartXValue](./) instance of the [ChartXValueType.Double](../chartxvaluetype/#Double) type. |
|[ fromMultilevelValue(value)](./fromMultilevelValue/#chartmultilevelvalue) | Creates a [ChartXValue](./) instance of the [ChartXValueType.Multilevel](../chartxvaluetype/#Multilevel) type. |
|[ fromString(value)](./fromString/#string) | Creates a [ChartXValue](./) instance of the [ChartXValueType.String](../chartxvaluetype/#String) type. |
|[ fromTimeSpan(value)](./fromTimeSpan/#unknown) | Creates a [ChartXValue](./) instance of the [ChartXValueType.Time](../chartxvaluetype/#Time) type. |

### Examples

Shows how to populate chart series with data.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

let shape = builder.insertChart(aw.Drawing.Charts.ChartType.Column, 432, 252);
let chart = shape.chart;
let series1 = chart.series.at(0);

// Clear X and Y values of the first series.
series1.clearValues();

// Populate the series with data.
series1.add(aw.Drawing.Charts.ChartXValue.fromDouble(3), aw.Drawing.Charts.ChartYValue.fromDouble(10), 10);
series1.add(aw.Drawing.Charts.ChartXValue.fromDouble(5), aw.Drawing.Charts.ChartYValue.fromDouble(5));
series1.add(aw.Drawing.Charts.ChartXValue.fromDouble(7), aw.Drawing.Charts.ChartYValue.fromDouble(11));
series1.add(aw.Drawing.Charts.ChartXValue.fromDouble(9));

let series2 = chart.series.at(1);
// Clear X and Y values of the second series.
series2.clear();

// Populate the series with data.
series2.add(aw.Drawing.Charts.ChartXValue.fromDouble(2), aw.Drawing.Charts.ChartYValue.fromDouble(4));
series2.add(aw.Drawing.Charts.ChartXValue.fromDouble(4), aw.Drawing.Charts.ChartYValue.fromDouble(7));
series2.add(aw.Drawing.Charts.ChartXValue.fromDouble(6), aw.Drawing.Charts.ChartYValue.fromDouble(14));
series2.add(aw.Drawing.Charts.ChartXValue.fromDouble(8), aw.Drawing.Charts.ChartYValue.fromDouble(7));

doc.save(base.artifactsDir + "Charts.PopulateChartWithData.docx");
```

### See Also

* module [Aspose.Words.Drawing.Charts](../)

