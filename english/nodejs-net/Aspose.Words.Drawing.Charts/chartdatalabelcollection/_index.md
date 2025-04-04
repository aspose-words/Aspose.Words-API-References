---
title: ChartDataLabelCollection class
linktitle: ChartDataLabelCollection class
articleTitle: ChartDataLabelCollection class
second_title: Aspose.Words for Node.js
description: "Aspose.Words.Drawing.Charts.ChartDataLabelCollection class. Represents a collection of [ChartDataLabel](../chartdatalabel/)"
type: docs
weight: 190
url: /nodejs-net/aspose.words.drawing.charts/chartdatalabelcollection/
---

## ChartDataLabelCollection class

Represents a collection of [ChartDataLabel](../chartdatalabel/).
To learn more, visit the [Working with Charts](https://docs.aspose.com/words/nodejs-net/working-with-charts/) documentation article.




### Properties

| Name | Description |
| --- | --- |
| [count](./count/) | Returns the number of [ChartDataLabel](../chartdatalabel/) in this collection. |
| [font](./font/) | Provides access to the font formatting of the data labels of the entire series. |
| [format](./format/) | Provides access to fill and line formatting of the data labels. |
| [numberFormat](./numberFormat/) | Gets an [ChartNumberFormat](../chartnumberformat/) instance allowing to set number format for the data labels of the entire series. |
| [orientation](./orientation/) | Gets or sets the text orientation of the data labels of the entire series. |
| [position](./position/) | Gets or sets the position of the data labels. |
| [rotation](./rotation/) | Gets or sets the rotation of the data labels of the entire series in degrees. |
| [separator](./separator/) | Gets or sets string separator used for the data labels of the entire series.  The default is a comma, except for pie charts showing only category name and percentage, when a line break  shall be used instead. |
| [showBubbleSize](./showBubbleSize/) | Allows to specify whether bubble size is to be displayed for the data labels of the entire series. Applies only to Bubble charts.  Default value is ``false``. |
| [showCategoryName](./showCategoryName/) | Allows to specify whether category name is to be displayed for the data labels of the entire series. Default value is ``false``. |
| [showDataLabelsRange](./showDataLabelsRange/) | Allows to specify whether values from data labels range to be displayed in the data labels of the entire series. Default value is ``false``. |
| [showLeaderLines](./showLeaderLines/) | Allows to specify whether data label leader lines need be shown for the data labels of the entire series. Default value is ``false``. |
| [showLegendKey](./showLegendKey/) | Allows to specify whether legend key is to be displayed for the data labels of the entire series. Default value is ``false``. |
| [showPercentage](./showPercentage/) | Allows to specify whether percentage value is to be displayed for the data labels of the entire series. Default value is ``false``. Applies only to Pie charts. |
| [showSeriesName](./showSeriesName/) | Returns or sets a Boolean to indicate the series name display behavior for the data labels of the entire series. ``true`` to show the series name; ``false`` to hide. By default ``false``. |
| [showValue](./showValue/) | Allows to specify whether values are to be displayed in the data labels of the entire series. Default value is ``false``. |
| [this[]](./this[]/) |  |

### Methods

| Name | Description |
| --- | --- |
|[ clearFormat()](./clearFormat/#default) | Clears format of all [ChartDataLabel](../chartdatalabel/) in this collection. |

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

* module [Aspose.Words.Drawing.Charts](../)

