﻿---
title: Stroke.backColor property
linktitle: backColor property
articleTitle: backColor property
second_title: Aspose.Words for Node.js
description: "Stroke.backColor property. Gets or sets the background color of the stroke."
type: docs
weight: 10
url: /nodejs-net/aspose.words.drawing/stroke/backColor/
---

## Stroke.backColor property

Gets or sets the background color of the stroke.


```js
get backColor(): string
```

### Remarks

The default value for a [Shape](../../shape/) is
white.



### Examples

Show how to set marker formatting.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

let shape = builder.insertChart(aw.Drawing.Charts.ChartType.Scatter, 432, 252);
let chart = shape.chart;

// Delete default generated series.
chart.series.clear();
let series = chart.series.add("AW Series 1", [ 0.7, 1.8, 2.6, 3.9 ],
  [ 2.7, 3.2, 0.8, 1.7 ]);

// Set marker formatting.
series.marker.size = 40;
series.marker.symbol = aw.Drawing.Charts.MarkerSymbol.Square;
let dataPoints = series.dataPoints;
dataPoints.at(0).marker.format.fill.presetTextured(aw.Drawing.PresetTexture.Denim);
dataPoints.at(0).marker.format.stroke.foreColor = "#FFFF00";
dataPoints.at(0).marker.format.stroke.backColor = "#FF0000";
dataPoints.at(1).marker.format.fill.presetTextured(aw.Drawing.PresetTexture.WaterDroplets);
dataPoints.at(1).marker.format.stroke.foreColor = "#FFFF00";
dataPoints.at(1).marker.format.stroke.visible = false;
dataPoints.at(2).marker.format.fill.presetTextured(aw.Drawing.PresetTexture.GreenMarble);
dataPoints.at(2).marker.format.stroke.foreColor = "#FFFF00";
dataPoints.at(3).marker.format.fill.presetTextured(aw.Drawing.PresetTexture.Oak);
dataPoints.at(3).marker.format.stroke.foreColor = "#FFFF00";
dataPoints.at(3).marker.format.stroke.transparency = 0.5;

doc.save(base.artifactsDir + "Charts.MarkerFormatting.docx");
```

### See Also

* module [Aspose.Words.Drawing](../../)
* class [Stroke](../)

