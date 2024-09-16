---
title: DocumentBuilder.insert_chart method
linktitle: insert_chart method
articleTitle: insert_chart method
second_title: Aspose.Words for Python
description: "aspose.words.DocumentBuilder.insert_chart method"
type: docs
weight: 280
url: /python-net/aspose.words/documentbuilder/insert_chart/
---

## insert_chart(chart_type, width, height) {#charttype_float_float}

Inserts an chart object into the document and scales it to the specified size.


```python
def insert_chart(self, chart_type: aspose.words.drawing.charts.ChartType, width: float, height: float):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| chart_type | [ChartType](../../../aspose.words.drawing.charts/charttype/) | The chart type to insert into the document. |
| width | float | The width of the image in points. Can be a negative or zero value to request 100% scale. |
| height | float | The height of the image in points. Can be a negative or zero value to request 100% scale. |

### Remarks

You can change the image size, location, positioning method and other settings using the 
[Shape](../../../aspose.words.drawing/shape/) object returned by this method.




### Returns

The image node that was just inserted.


## insert_chart(chart_type, horz_pos, left, vert_pos, top, width, height, wrap_type) {#charttype_relativehorizontalposition_float_relativeverticalposition_float_float_float_wraptype}

Inserts an chart object into the document and scales it to the specified size.


```python
def insert_chart(self, chart_type: aspose.words.drawing.charts.ChartType, horz_pos: aspose.words.drawing.RelativeHorizontalPosition, left: float, vert_pos: aspose.words.drawing.RelativeVerticalPosition, top: float, width: float, height: float, wrap_type: aspose.words.drawing.WrapType):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| chart_type | [ChartType](../../../aspose.words.drawing.charts/charttype/) | The chart type to insert into the document. |
| horz_pos | [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/) | Specifies where the distance to the image is measured from. |
| left | float | Distance in points from the origin to the left side of the image. |
| vert_pos | [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/) | Specifies where the distance to the image measured from. |
| top | float | Distance in points from the origin to the top side of the image. |
| width | float | The width of the image in points. Can be a negative or zero value to request 100% scale. |
| height | float | The height of the image in points. Can be a negative or zero value to request 100% scale. |
| wrap_type | [WrapType](../../../aspose.words.drawing/wraptype/) | Specifies how to wrap text around the image. |

### Remarks

You can change the image size, location, positioning method and other settings using the 
[Shape](../../../aspose.words.drawing/shape/) object returned by this method.




### Returns

The image node that was just inserted.


## Examples

Shows how to insert a pie chart into a document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
chart = builder.insert_chart(chart_type=aw.drawing.charts.ChartType.PIE, width=aw.ConvertUtil.pixel_to_point(pixels=300), height=aw.ConvertUtil.pixel_to_point(pixels=300)).chart
chart.series.clear()
chart.series.add(series_name='My fruit', categories=['Apples', 'Bananas', 'Cherries'], values=[1.3, 2.2, 1.5])
doc.save(file_name=ARTIFACTS_DIR + 'DocumentBuilder.InsertPieChart.docx')
```

Shows how to specify position and wrapping while inserting a chart.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.insert_chart(chart_type=aw.drawing.charts.ChartType.PIE, horz_pos=aw.drawing.RelativeHorizontalPosition.MARGIN, left=100, vert_pos=aw.drawing.RelativeVerticalPosition.MARGIN, top=100, width=200, height=100, wrap_type=aw.drawing.WrapType.SQUARE)
doc.save(file_name=ARTIFACTS_DIR + 'DocumentBuilder.InsertedChartRelativePosition.docx')
```

## See Also

* module [aspose.words](../../)
* class [DocumentBuilder](../)

