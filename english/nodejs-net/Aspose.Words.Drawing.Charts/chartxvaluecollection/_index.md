---
title: ChartXValueCollection class
linktitle: ChartXValueCollection class
articleTitle: ChartXValueCollection class
second_title: Aspose.Words for Node.js
description: "Aspose.Words.Drawing.Charts.ChartXValueCollection class. Represents a collection of X values for a chart series."
type: docs
weight: 410
url: /nodejs-net/aspose.words.drawing.charts/chartxvaluecollection/
---

## ChartXValueCollection class

Represents a collection of X values for a chart series.


### Remarks

All items of the collection other than **null** must have the same [ChartXValue.valueType](../chartxvalue/valueType/).

The collection allows only changing X values. To add or insert new values to a chart series, or remove values,
the appropriate methods of the [ChartSeries](../chartseries/) class can be used.




### Properties

| Name | Description |
| --- | --- |
| [count](./count/) | Gets the number of items in this collection. |
| [formatCode](./formatCode/) | Gets or sets the format code applied to the X values. |
| [this[]](./this[]/) |  |

### Examples

Shows how to get chart series data.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder();

let shape = builder.insertChart(aw.Drawing.Charts.ChartType.Column, 432, 252);
let chart = shape.chart;
let series = chart.series.at(0);

const minValue = -1.7976931348623157E+308;
const minValueIndex = 0;
const maxValue = 1.7976931348623157E+308;
const maxValueIndex = 0;

for (var i = 0; i < series.yvalues.count; i++)
{
  // Clear individual format of all data points.
  // Data points and data values are one-to-one in column charts.
  series.dataPoints.at(i).clearFormat();

  // Get Y value.
  let yValue = series.yvalues.at(i).doubleValue;

  if (yValue < minValue)
  {
    minValue = yValue;
    minValueIndex = i;
  }

  if (yValue > maxValue)
  {
    maxValue = yValue;
    maxValueIndex = i;
  }
}

// Change colors of the max and min values.
series.dataPoints.at(minValueIndex).format.fill.foreColor = "#FF0000";
series.dataPoints.at(maxValueIndex).format.fill.foreColor = "#008000";

doc.save(base.artifactsDir + "Charts.GetChartSeriesData.docx");
```

### See Also

* module [Aspose.Words.Drawing.Charts](../)
* method [ChartSeries.add()](../chartseries/add/#chartxvalue_chartyvalue)
* method [ChartSeries.add()](../chartseries/add/#chartxvalue_chartyvalue_number)
* method [ChartSeries.insert()](../chartseries/insert/#number_chartxvalue_chartyvalue)
* method [ChartSeries.insert()](../chartseries/insert/#number_chartxvalue_chartyvalue_number)
* method [ChartSeries.remove()](../chartseries/remove/#number)

