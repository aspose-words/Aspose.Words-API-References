---
title: ChartFormat.shape_type property
linktitle: shape_type property
articleTitle: shape_type property
second_title: Aspose.Words for Python
description: "ChartFormat.shape_type property. Gets or sets the shape type of the parent chart element."
type: docs
weight: 30
url: /python-net/aspose.words.drawing.charts/chartformat/shape_type/
---

## ChartFormat.shape_type property

Gets or sets the shape type of the parent chart element.


```python
@property
def shape_type(self) -> aspose.words.drawing.charts.ChartShapeType:
    ...

@shape_type.setter
def shape_type(self, value: aspose.words.drawing.charts.ChartShapeType):
    ...

```

### Remarks

Currently, the property can only be used for data labels.


### Examples

Shows how to set fill, stroke and callout formatting for chart data labels.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
shape = builder.insert_chart(chart_type=aw.drawing.charts.ChartType.COLUMN, width=432, height=252)
chart = shape.chart
# Delete default generated series.
chart.series.clear()
# Add new series.
series = chart.series.add1(series_name='AW Series 1', categories=['AW Category 1', 'AW Category 2', 'AW Category 3', 'AW Category 4'], values=[100, 200, 300, 400])
# Show data labels.
series.has_data_labels = True
series.data_labels.show_value = True
# Format data labels as callouts.
format = series.data_labels.format
format.shape_type = aw.drawing.charts.ChartShapeType.WEDGE_RECT_CALLOUT
format.stroke.color = aspose.pydrawing.Color.dark_green
format.fill.solid(aspose.pydrawing.Color.green)
series.data_labels.font.color = aspose.pydrawing.Color.yellow
# Change fill and stroke of an individual data label.
label_format = series.data_labels[0].format
label_format.stroke.color = aspose.pydrawing.Color.dark_blue
label_format.fill.solid(aspose.pydrawing.Color.blue)
doc.save(file_name=ARTIFACTS_DIR + 'Charts.FormatDataLables.docx')
```

### See Also

* module [aspose.words.drawing.charts](../../)
* class [ChartFormat](../)

