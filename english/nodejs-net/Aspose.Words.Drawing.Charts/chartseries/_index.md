---
title: ChartSeries class
linktitle: ChartSeries class
articleTitle: ChartSeries class
second_title: Aspose.Words for Node.js
description: "Aspose.Words.Drawing.Charts.ChartSeries class. Represents chart series properties"
type: docs
weight: 320
url: /nodejs-net/aspose.words.drawing.charts/chartseries/
---

## ChartSeries class

Represents chart series properties.
To learn more, visit the [Working with Charts](https://docs.aspose.com/words/nodejs-net/working-with-charts/) documentation article.




### Properties

| Name | Description |
| --- | --- |
| [bubble3D](./bubble3D/) | Specifies whether the bubbles in Bubble chart should have a 3-D effect applied to them. |
| [bubbleSizes](./bubbleSizes/) | Gets a collection of bubble sizes for this chart series. |
| [dataLabels](./dataLabels/) | Specifies the settings for the data labels for the entire series. |
| [dataPoints](./dataPoints/) | Returns a collection of formatting objects for all data points in this series. |
| [explosion](./explosion/) | Specifies the amount the data point shall be moved from the center of the pie. Can be negative, negative means that property is not set and no explosion should be applied. Applies only to Pie charts. |
| [format](./format/) | Provides access to fill and line formatting of the series. |
| [hasDataLabels](./hasDataLabels/) | Gets or sets a flag indicating whether data labels are displayed for the series. |
| [invertIfNegative](./invertIfNegative/) | Specifies whether the parent element shall inverts its colors if the value is negative. |
| [legendEntry](./legendEntry/) | Gets a legend entry for this chart series. |
| [marker](./marker/) | Specifies a data marker. Marker is automatically created when requested. |
| [name](./name/) | Gets or sets the name of the series, if name is not set explicitly it is generated using index. By default returns Series plus one based index. |
| [seriesType](./seriesType/) | Gets the type of this chart series. |
| [smooth](./smooth/) | Allows to specify whether the line connecting the points on the chart shall be smoothed using Catmull-Rom splines. |
| [xvalues](./xvalues/) | Gets a collection of X values for this chart series. |
| [yvalues](./yvalues/) | Gets a collection of Y values for this chart series. |

### Methods

| Name | Description |
| --- | --- |
|[ add(xValue)](./add/#chartxvalue) | Adds the specified X value to the chart series. If the series supports Y values and bubble sizes, they will be empty for the X value. |
|[ add(xValue, yValue)](./add/#chartxvalue_chartyvalue) | Adds the specified X and Y values to the chart series. |
|[ add(xValue, yValue, bubbleSize)](./add/#chartxvalue_chartyvalue_number) | Adds the specified X value, Y value and bubble size to the chart series. |
|[ clear()](./clear/#default) | Removes all data values from the chart series. Format of all individual data points and data labels is cleared. |
|[ clearValues()](./clearValues/#default) | Removes all data values from the chart series with preserving the format of the data points and data labels. |
|[ copyFormatFrom(dataPointIndex)](./copyFormatFrom/#number) | Copies default data point format from the data point with the specified index. |
|[ insert(index, xValue)](./insert/#number_chartxvalue) | Inserts the specified X value into the chart series at the specified index. If the series supports Y values and bubble sizes, they will be empty for the X value. |
|[ insert(index, xValue, yValue)](./insert/#number_chartxvalue_chartyvalue) | Inserts the specified X and Y values into the chart series at the specified index. |
|[ insert(index, xValue, yValue, bubbleSize)](./insert/#number_chartxvalue_chartyvalue_number) | Inserts the specified X value, Y value and bubble size into the chart series at the specified index. |
|[ remove(index)](./remove/#number) | Removes the X value, Y value, and bubble size, if supported, from the chart series at the specified index. The corresponding data point and data label are also removed. |

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

* module [Aspose.Words.Drawing.Charts](../)

