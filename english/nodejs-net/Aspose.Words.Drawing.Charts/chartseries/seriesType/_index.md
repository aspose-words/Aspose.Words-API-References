---
title: ChartSeries.seriesType property
linktitle: seriesType property
articleTitle: seriesType property
second_title: Aspose.Words for Node.js
description: "ChartSeries.seriesType property. Gets the type of this chart series."
type: docs
weight: 120
url: /nodejs-net/aspose.words.drawing.charts/chartseries/seriesType/
---

## ChartSeries.seriesType property

Gets the type of this chart series.


```js
get seriesType(): Aspose.Words.Drawing.Charts.ChartSeriesType
```

### Examples

Shows how to remove specific chart serie.

```js
let doc = new aw.Document(base.myDir + "Reporting engine template - Chart series.docx");
let chart = doc.getShape(0, true).chart;

// Remove all series of the Column type.
for (var i = chart.series.count - 1; i >= 0; i--)
{
  if (chart.series.at(i).seriesType == aw.Drawing.Charts.ChartSeriesType.Column)
    chart.series.removeAt(i);
}

chart.series.add(
  "Aspose Series",
  [ "Category 1", "Category 2", "Category 3", "Category 4" ],
  [ 5.6, 7.1, 2.9, 8.9 ]);

doc.save(base.artifactsDir + "Charts.RemoveSpecificChartSeries.docx");
```

### See Also

* module [Aspose.Words.Drawing.Charts](../../)
* class [ChartSeries](../)

