---
title: ChartDataLabel.showLegendKey property
linktitle: showLegendKey property
articleTitle: showLegendKey property
second_title: Aspose.Words for NodeJs
description: "ChartDataLabel.showLegendKey property. Allows to specify if legend key is to be displayed for the data labels on a chart"
type: docs
weight: 170
url: /nodejs-net/Aspose.Words.Drawing.Charts/chartdatalabel/showLegendKey/
---

## ChartDataLabel.showLegendKey property

Allows to specify if legend key is to be displayed for the data labels on a chart. 
Default value is ``false``.



```js
get showLegendKey(): boolean
```

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

  // For a cleaner looking graph, we can remove data labels individually.
  chart.series.at(1).dataLabels.at(2).clearFormat();

  // We can also strip an entire series of its data labels at once.
  chart.series.at(2).dataLabels.clearFormat();

  doc.save(base.artifactsDir + "Charts.dataLabels.docx");
});
```

### See Also

* module [Aspose.Words.Drawing.Charts](../../)
* class [ChartDataLabel](../)

