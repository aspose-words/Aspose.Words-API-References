---
title: ChartDataLabel class
linktitle: ChartDataLabel class
articleTitle: ChartDataLabel class
second_title: Aspose.Words for Node.js
description: "Aspose.Words.Drawing.Charts.ChartDataLabel class. Represents data label on a chart point or trendline"
type: docs
weight: 180
url: /nodejs-net/aspose.words.drawing.charts/chartdatalabel/
---

## ChartDataLabel class

Represents data label on a chart point or trendline.
To learn more, visit the [Working with Charts](https://docs.aspose.com/words/nodejs-net/working-with-charts/) documentation article.




### Remarks

On a series, the [ChartDataLabel](./) object is a member of the [ChartDataLabelCollection](../chartdatalabelcollection/). 
The [ChartDataLabelCollection](../chartdatalabelcollection/) contains a [ChartDataLabel](./) object for each point. 



### Properties

| Name | Description |
| --- | --- |
| [font](./font/) | Provides access to the font formatting of this data label. |
| [format](./format/) | Provides access to fill and line formatting of the data label. |
| [index](./index/) | Specifies the index of the containing element.  This index shall determine which of the parent's children collection this element applies to. Default value is 0. |
| [isHidden](./isHidden/) | Gets/sets a flag indicating whether this label is hidden. The default value is ``false``. |
| [isVisible](./isVisible/) | Returns ``true`` if this data label has something to display. |
| [left](./left/) | Gets or sets the distance of the data label in points from the left edge of the chart or from the position specified by its [ChartDataLabel.position](./position/) property, depending on the value of the [ChartDataLabel.leftMode](./leftMode/) property. |
| [leftMode](./leftMode/) | Gets or sets the interpretation mode of the [ChartDataLabel.left](./left/) property value: whether it sets the location of the data label from the left edge of the chart of from the position specified by its [ChartDataLabel.position](./position/) property. |
| [numberFormat](./numberFormat/) | Returns number format of the parent element. |
| [orientation](./orientation/) | Gets or sets the orientation of the label text. |
| [position](./position/) | Gets or sets the position of the data label. |
| [rotation](./rotation/) | Gets or sets the rotation of the label in degrees. |
| [separator](./separator/) | Gets or sets string separator used for the data labels on a chart.  The default is a comma, except for pie charts showing only category name and percentage, when a line break  shall be used instead. |
| [showBubbleSize](./showBubbleSize/) | Allows to specify if bubble size is to be displayed for the data labels on a chart.  Applies only to Bubble charts.  Default value is ``false``. |
| [showCategoryName](./showCategoryName/) | Allows to specify if category name is to be displayed for the data labels on a chart.  Default value is ``false``. |
| [showDataLabelsRange](./showDataLabelsRange/) | Allows to specify if values from data labels range to be displayed in the data labels.  Default value is ``false``. |
| [showLeaderLines](./showLeaderLines/) | Allows to specify if data label leader lines need be shown.  Default value is ``false``. |
| [showLegendKey](./showLegendKey/) | Allows to specify if legend key is to be displayed for the data labels on a chart.  Default value is ``false``. |
| [showPercentage](./showPercentage/) | Allows to specify if percentage value is to be displayed for the data labels on a chart.  Default value is ``false``. |
| [showSeriesName](./showSeriesName/) | Returns or sets a Boolean to indicate the series name display behavior for the data labels on a chart.  ``true`` to show the series name; ``false`` to hide. By default ``false``. |
| [showValue](./showValue/) | Allows to specify if values are to be displayed in the data labels.  Default value is ``false``. |
| [top](./top/) | Gets or sets the distance of the data label in points from the top edge of the chart or from the position specified by its [ChartDataLabel.position](./position/) property, depending on the value of the [ChartDataLabel.topMode](./topMode/) property. |
| [topMode](./topMode/) | Gets or sets the interpretation mode of the [ChartDataLabel.top](./top/) property value: whether it sets the location of the data label from the top edge of the chart of from the position specified by its [ChartDataLabel.position](./position/) property. |

### Methods

| Name | Description |
| --- | --- |
|[ clearFormat()](./clearFormat/#default) | Clears format of this data label. The properties are set to the default values defined in the parent data label collection. |

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

