---
title: ChartDataLabel.left property
linktitle: left property
articleTitle: left property
second_title: Aspose.Words for Node.js
description: "ChartDataLabel.left property. Gets or sets the distance of the data label in points from the left edge of the chart or from the position specified by its [ChartDataLabel.position](../position/) property, depending on the value of the [ChartDataLabel.leftMode](../leftMode/) property."
type: docs
weight: 60
url: /nodejs-net/aspose.words.drawing.charts/chartdatalabel/left/
---

## ChartDataLabel.left property

Gets or sets the distance of the data label in points from the left edge of the chart or from the position
specified by its [ChartDataLabel.position](../position/) property, depending on the value of the [ChartDataLabel.leftMode](../leftMode/)
property.



```js
get left(): number
```

### Remarks

The value of the property changes proportionally if the chart shape is resized.

The property cannot be set in a Word 2016 chart.




### Examples

Shows how to place data labels of doughnut chart outside doughnut.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

const chartWidth = 432;
const  chartHeight = 252;
let shape = builder.insertChart(aw.Drawing.Charts.ChartType.Doughnut, chartWidth, chartHeight);
let chart = shape.chart;
let seriesColl = chart.series;
// Delete default generated series.
seriesColl.clear();

// Hide the legend.
chart.legend.position = aw.Drawing.Charts.LegendPosition.None;

// Generate data.
const dataLength = 20;
let totalValue = 0;
let categories = [];
let values = [];

for (let i = 0; i < dataLength; i++)
{
  categories.push(`Category ${i}`);
  values.push(dataLength - i);
  totalValue = totalValue + values.at(i);
}

let series = seriesColl.add("Series 1", categories, values);
series.hasDataLabels = true;

let dataLabels = series.dataLabels;
dataLabels.showValue = true;
dataLabels.showLeaderLines = true;

// The Position property cannot be used for doughnut charts. Let's place data labels using the Left and Top
// properties around a circle outside of the chart doughnut.
// The origin is in the upper left corner of the chart.

const titleAreaHeight = 25.5; // This can be calculated using title text and font.
const doughnutCenterY = titleAreaHeight + (chartHeight - titleAreaHeight) / 2;
const doughnutCenterX = chartWidth / 2;
const labelHeight = 16.5; // This can be calculated using label font.
const oneCharLabelWidth = 12.75; // This can be calculated for each label using its text and font.
const twoCharLabelWidth = 17.25; // This can be calculated for each label using its text and font.
const yMargin = 0.75;
const labelMargin = 1.5;
const labelCircleRadius = chartHeight - doughnutCenterY - yMargin - labelHeight / 2;

// Because the data points start at the top, the X coordinates used in the Left and Top properties of
// the data labels point to the right and the Y coordinates point down, the starting angle is -PI/2.
let totalAngle = -Math.PI / 2;
let previousLabel = null;

for (let i = 0; i < series.yvalues.count; i++)
{
  let dataLabel = dataLabels.at(i);

  let value = series.yvalues.at(i).doubleValue;
  let labelWidth;
  if (value < 10)
    labelWidth = oneCharLabelWidth;
  else
    labelWidth = twoCharLabelWidth;
  let labelSegmentAngle = value / totalValue * 2 * Math.PI;
  let labelAngle = labelSegmentAngle / 2 + totalAngle;
  let labelCenterX = labelCircleRadius * Math.cos(labelAngle) + doughnutCenterX;
  let labelCenterY = labelCircleRadius * Math.sin(labelAngle) + doughnutCenterY;
  let labelLeft = labelCenterX - labelWidth / 2;
  let labelTop = labelCenterY - labelHeight / 2;

  // If the current data label overlaps other labels, move it horizontally.
  if ((previousLabel != null) &&
    (Math.abs(previousLabel.top - labelTop) < labelHeight) &&
    (Math.abs(previousLabel.left - labelLeft) < labelWidth))
  {
    // Move right on the top, left on the bottom.
    let isOnTop = (totalAngle < 0) || (totalAngle >= Math.PI);
    let factor;
    if (isOnTop)
      factor = 1;
    else
      factor = -1;

    labelLeft = previousLabel.left + labelWidth * factor + labelMargin;
  }

  dataLabel.left = labelLeft;
  dataLabel.leftMode = aw.Drawing.Charts.ChartDataLabelLocationMode.Absolute;
  dataLabel.top = labelTop;
  dataLabel.topMode = aw.Drawing.Charts.ChartDataLabelLocationMode.Absolute;

  totalAngle = totalAngle + labelSegmentAngle;
  previousLabel = dataLabel;
}

doc.save(base.artifactsDir + "Charts.DoughnutChartLabelPosition.docx");
```

### See Also

* module [Aspose.Words.Drawing.Charts](../../)
* class [ChartDataLabel](../)

