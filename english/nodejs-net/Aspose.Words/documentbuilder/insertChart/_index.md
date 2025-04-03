---
title: DocumentBuilder.insertChart method
linktitle: insertChart method
articleTitle: insertChart method
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.DocumentBuilder.insertChart method"
type: docs
weight: 280
url: /nodejs-net/aspose.words/documentbuilder/insertChart/
---

## insertChart(chartType, width, height) {#charttype_number_number}

Inserts an chart object into the document and scales it to the specified size.


```js
insertChart(chartType: Aspose.Words.Drawing.Charts.ChartTypewidth: numberheight: number)
```

| Parameter | Type | Description |
| --- | --- | --- |
| chartType | [ChartType](../../../aspose.words.drawing.charts/charttype/) | The chart type to insert into the document. |
| width | number | The width of the image in points. Can be a negative or zero value to request 100% scale. |
| height | number | The height of the image in points. Can be a negative or zero value to request 100% scale. |

### Remarks

You can change the image size, location, positioning method and other settings using the 
[Shape](../../../aspose.words.drawing/shape/) object returned by this method.




### Returns

The image node that was just inserted.


## insertChart(chartType, horzPos, left, vertPos, top, width, height, wrapType) {#charttype_relativehorizontalposition_number_relativeverticalposition_number_number_number_wraptype}

Inserts an chart object into the document and scales it to the specified size.


```js
insertChart(chartType: Aspose.Words.Drawing.Charts.ChartTypehorzPos: Aspose.Words.Drawing.RelativeHorizontalPositionleft: numbervertPos: Aspose.Words.Drawing.RelativeVerticalPositiontop: numberwidth: numberheight: numberwrapType: Aspose.Words.Drawing.WrapType)
```

| Parameter | Type | Description |
| --- | --- | --- |
| chartType | [ChartType](../../../aspose.words.drawing.charts/charttype/) | The chart type to insert into the document. |
| horzPos | [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/) | Specifies where the distance to the image is measured from. |
| left | number | Distance in points from the origin to the left side of the image. |
| vertPos | [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/) | Specifies where the distance to the image measured from. |
| top | number | Distance in points from the origin to the top side of the image. |
| width | number | The width of the image in points. Can be a negative or zero value to request 100% scale. |
| height | number | The height of the image in points. Can be a negative or zero value to request 100% scale. |
| wrapType | [WrapType](../../../aspose.words.drawing/wraptype/) | Specifies how to wrap text around the image. |

### Remarks

You can change the image size, location, positioning method and other settings using the 
[Shape](../../../aspose.words.drawing/shape/) object returned by this method.




### Returns

The image node that was just inserted.


## Examples

Shows how to insert a pie chart into a document.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

let chart = builder.insertChart(aw.Drawing.Charts.ChartType.Pie, aw.ConvertUtil.pixelToPoint(300), 
  aw.ConvertUtil.pixelToPoint(300)).chart;
expect(aw.ConvertUtil.pixelToPoint(300)).toEqual(225.0);
chart.series.clear();
chart.series.add("My fruit",
  [ "Apples", "Bananas", "Cherries" ],
  [ 1.3, 2.2, 1.5 ]);

doc.save(base.artifactsDir + "DocumentBuilder.InsertPieChart.docx");
```

Shows how to specify position and wrapping while inserting a chart.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

builder.insertChart(aw.Drawing.Charts.ChartType.Pie, aw.Drawing.RelativeHorizontalPosition.Margin, 100, aw.Drawing.RelativeVerticalPosition.Margin,
  100, 200, 100, aw.Drawing.WrapType.Square);

doc.save(base.artifactsDir + "DocumentBuilder.InsertedChartRelativePosition.docx");
```

## See Also

* module [Aspose.Words](../../)
* class [DocumentBuilder](../)

