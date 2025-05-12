---
title: ChartDataLabelCollection.position property
linktitle: position property
articleTitle: position property
second_title: Aspose.Words for Node.js
description: "ChartDataLabelCollection.position property. Gets or sets the position of the data labels."
type: docs
weight: 60
url: /nodejs-net/aspose.words.drawing.charts/chartdatalabelcollection/position/
---

## ChartDataLabelCollection.position property

Gets or sets the position of the data labels.


```js
get position(): Aspose.Words.Drawing.Charts.ChartDataLabelPosition
```

### Remarks

The position can be set for data labels of the following chart series types:

- [ChartSeriesType.Bar](../../chartseriestype/#Bar), [ChartSeriesType.Column](../../chartseriestype/#Column),
[ChartSeriesType.Histogram](../../chartseriestype/#Histogram), [ChartSeriesType.Pareto](../../chartseriestype/#Pareto),
[ChartSeriesType.Waterfall](../../chartseriestype/#Waterfall); allowed values: [ChartDataLabelPosition.Center](../../chartdatalabelposition/#Center),
[ChartDataLabelPosition.InsideBase](../../chartdatalabelposition/#InsideBase), [ChartDataLabelPosition.InsideEnd](../../chartdatalabelposition/#InsideEnd) and
[ChartDataLabelPosition.OutsideEnd](../../chartdatalabelposition/#OutsideEnd);

- [ChartSeriesType.BarStacked](../../chartseriestype/#BarStacked), [ChartSeriesType.BarPercentStacked](../../chartseriestype/#BarPercentStacked),
[ChartSeriesType.ColumnStacked](../../chartseriestype/#ColumnStacked), [ChartSeriesType.ColumnPercentStacked](../../chartseriestype/#ColumnPercentStacked); allowed
values: [ChartDataLabelPosition.Center](../../chartdatalabelposition/#Center), [ChartDataLabelPosition.InsideBase](../../chartdatalabelposition/#InsideBase)
and [ChartDataLabelPosition.InsideEnd](../../chartdatalabelposition/#InsideEnd);

- [ChartSeriesType.Bubble](../../chartseriestype/#Bubble), [ChartSeriesType.Bubble3D](../../chartseriestype/#Bubble3D),
[ChartSeriesType.Line](../../chartseriestype/#Line), [ChartSeriesType.LineStacked](../../chartseriestype/#LineStacked),
[ChartSeriesType.LinePercentStacked](../../chartseriestype/#LinePercentStacked), [ChartSeriesType.Scatter](../../chartseriestype/#Scatter),
[ChartSeriesType.Stock](../../chartseriestype/#Stock); allowed values: [ChartDataLabelPosition.Center](../../chartdatalabelposition/#Center),
[ChartDataLabelPosition.Left](../../chartdatalabelposition/#Left), [ChartDataLabelPosition.Right](../../chartdatalabelposition/#Right),
[ChartDataLabelPosition.Above](../../chartdatalabelposition/#Above) and [ChartDataLabelPosition.Below](../../chartdatalabelposition/#Below);

- [ChartSeriesType.Pie](../../chartseriestype/#Pie), [ChartSeriesType.Pie3D](../../chartseriestype/#Pie3D),
[ChartSeriesType.PieOfBar](../../chartseriestype/#PieOfBar), [ChartSeriesType.PieOfPie](../../chartseriestype/#PieOfPie); allowed values:
[ChartDataLabelPosition.Center](../../chartdatalabelposition/#Center), [ChartDataLabelPosition.InsideEnd](../../chartdatalabelposition/#InsideEnd),
[ChartDataLabelPosition.OutsideEnd](../../chartdatalabelposition/#OutsideEnd) and [ChartDataLabelPosition.BestFit](../../chartdatalabelposition/#BestFit);

- [ChartSeriesType.BoxAndWhisker](../../chartseriestype/#BoxAndWhisker); allowed values:
[ChartDataLabelPosition.Left](../../chartdatalabelposition/#Left), [ChartDataLabelPosition.Right](../../chartdatalabelposition/#Right),
[ChartDataLabelPosition.Above](../../chartdatalabelposition/#Above) and [ChartDataLabelPosition.Below](../../chartdatalabelposition/#Below).




### Examples

Shows how to set the position of the data label.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

// Insert column chart.
let shape = builder.insertChart(aw.Drawing.Charts.ChartType.Column, 432, 252);
let chart = shape.chart;
let seriesColl = chart.series;

// Delete default generated series.
seriesColl.clear();

// Add series.
let series = seriesColl.add(
  "Series 1",
  [ "Category 1", "Category 2", "Category 3" ],
  [ 4, 5, 6 ]);

// Show data labels and set font color.
series.hasDataLabels = true;
let dataLabels = series.dataLabels;
dataLabels.showValue = true;
dataLabels.font.color = "#FFFFFF";

// Set data label position.
dataLabels.position = aw.Drawing.Charts.ChartDataLabelPosition.InsideBase;
dataLabels.at(0).position = aw.Drawing.Charts.ChartDataLabelPosition.OutsideEnd;
dataLabels.at(0).font.color = "#8B0000";

doc.save(base.artifactsDir + "Charts.labelPosition.docx");
```

### See Also

* module [Aspose.Words.Drawing.Charts](../../)
* class [ChartDataLabelCollection](../)

