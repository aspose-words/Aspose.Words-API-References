---
title: ChartDataLabel.showLeaderLines property
linktitle: showLeaderLines property
articleTitle: showLeaderLines property
second_title: Aspose.Words for Node.js
description: "ChartDataLabel.showLeaderLines property. Allows to specify if data label leader lines need be shown"
type: docs
weight: 160
url: /nodejs-net/aspose.words.drawing.charts/chartdatalabel/showLeaderLines/
---

## ChartDataLabel.showLeaderLines property

Allows to specify if data label leader lines need be shown. 
Default value is ``false``.



```js
get showLeaderLines(): boolean
```

### Remarks

Applies to Pie charts only. 
Leader lines create a visual connection between a data label and its corresponding data point.


### Examples

Shows how to apply labels to data points in a line chart.

```js
test('DataLabels', () => {
  let doc = new aw.Document();
  let builder = new aw.DocumentBuilder(doc);

  let chartShape = builder.insertChart(aw.Drawing.Charts.ChartType.Line, 400, 300);
  let chart = chartShape.chart;

  expect(chart.series.count).toEqual(3);
  expect(chart.series.at(0).name).toEqual("Series 1");
  expect(chart.series.at(1).name).toEqual("Series 2");
  expect(chart.series.at(2).name).toEqual("Series 3");

  // Apply data labels to every series in the chart.
  // These labels will appear next to each data point in the graph and display its value.
  for (let series of chart.series)
  {
    applyDataLabels(series, 4, "000.0", ", ");
    expect(series.dataLabels.count).toEqual(4);
  }

  // Change the separator string for every data label in a series.
  for (let label of chart.series.at(0).dataLabels)
  {
      expect(label.separator).toEqual(", ");
      label.separator = " & ";
  }

  let dataLabel = chart.series.at(1).dataLabels.at(2);
  dataLabel.format.fill.color = "#FF0000";

  // For a cleaner looking graph, we can remove data labels individually.
  dataLabel.clearFormat();

  // We can also strip an entire series of its data labels at once.
  chart.series.at(2).dataLabels.clearFormat();

  doc.save(base.artifactsDir + "Charts.dataLabels.docx");
});
```

### See Also

* module [Aspose.Words.Drawing.Charts](../../)
* class [ChartDataLabel](../)

