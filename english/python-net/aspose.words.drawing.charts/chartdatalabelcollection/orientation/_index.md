---
title: ChartDataLabelCollection.orientation property
linktitle: orientation property
articleTitle: orientation property
second_title: Aspose.Words for Python
description: "ChartDataLabelCollection.orientation property. Gets or sets the text orientation of the data labels of the entire series."
type: docs
weight: 60
url: /python-net/aspose.words.drawing.charts/chartdatalabelcollection/orientation/
---

## ChartDataLabelCollection.orientation property

Gets or sets the text orientation of the data labels of the entire series.


```python
@property
def orientation(self) -> aspose.words.drawing.ShapeTextOrientation:
    ...

@orientation.setter
def orientation(self, value: aspose.words.drawing.ShapeTextOrientation):
    ...

```

### Remarks

The default value is [ShapeTextOrientation.HORIZONTAL](../../../aspose.words.drawing/shapetextorientation/#HORIZONTAL).



### Examples

Shows how to change orientation and rotation for data labels.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
shape = builder.insert_chart(chart_type=aw.drawing.charts.ChartType.COLUMN, width=432, height=252)
series = shape.chart.series[0]
data_labels = series.data_labels
# Show data labels.
series.has_data_labels = True
data_labels.show_value = True
data_labels.show_category_name = True
# Define data label shape.
data_labels.format.shape_type = aw.drawing.charts.ChartShapeType.UP_ARROW
data_labels.format.stroke.fill.solid(aspose.pydrawing.Color.dark_blue)
# Set data label orientation and rotation for the entire series.
data_labels.orientation = aw.drawing.ShapeTextOrientation.VERTICAL_FAR_EAST
data_labels.rotation = -45
# Change orientation and rotation of the first data label.
data_labels[0].orientation = aw.drawing.ShapeTextOrientation.HORIZONTAL
data_labels[0].rotation = 45
doc.save(file_name=ARTIFACTS_DIR + 'Charts.LabelOrientationRotation.docx')
```

### See Also

* module [aspose.words.drawing.charts](../../)
* class [ChartDataLabelCollection](../)

