---
title: insert_chart method
second_title: Aspose.Words for Python via .NET API Reference
description: "aspose.words.DocumentBuilder.insert_chart method"
type: docs
weight: 260
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
| chart_type | [ChartType](../../../aspose.words.drawing.charts/charttype/) |  |
| width | float |  |
| height | float |  |

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
| chart_type | [ChartType](../../../aspose.words.drawing.charts/charttype/) |  |
| horz_pos | [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/) |  |
| left | float |  |
| vert_pos | [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/) |  |
| top | float |  |
| width | float |  |
| height | float |  |
| wrap_type | [WrapType](../../../aspose.words.drawing/wraptype/) |  |

You can change the image size, location, positioning method and other settings using the 
[Shape](../../../aspose.words.drawing/shape/) object returned by this method.




### Returns

The image node that was just inserted.


## Examples

Shows how to insert a pie chart into a document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

chart = builder.insert_chart(aw.drawing.charts.ChartType.PIE, aw.ConvertUtil.pixel_to_point(300),
    aw.ConvertUtil.pixel_to_point(300)).chart
chart.series.clear()
chart.series.add("My fruit",
    [ "Apples", "Bananas", "Cherries" ],
    [ 1.3, 2.2, 1.5 ])

doc.save(ARTIFACTS_DIR + "DocumentBuilder.insert_pie_chart.docx")
```

Shows how to specify position and wrapping while inserting a chart.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

builder.insert_chart(aw.drawing.charts.ChartType.PIE, aw.drawing.RelativeHorizontalPosition.MARGIN, 100, aw.drawing.RelativeVerticalPosition.MARGIN,
    100, 200, 100, aw.drawing.WrapType.SQUARE)

doc.save(ARTIFACTS_DIR + "DocumentBuilder.inserted_chart_relative_position.docx")
```

## See Also

* module [aspose.words](../../)
* class [DocumentBuilder](../)

