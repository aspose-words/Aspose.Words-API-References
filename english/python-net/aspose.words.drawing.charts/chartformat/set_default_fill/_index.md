---
title: ChartFormat.set_default_fill method
linktitle: set_default_fill method
articleTitle: set_default_fill method
second_title: Aspose.Words for Python
description: "ChartFormat.set_default_fill method. Resets the fill of the chart element to have the default value."
type: docs
weight: 50
url: /python-net/aspose.words.drawing.charts/chartformat/set_default_fill/
---

## set_default_fill() {#default}

Resets the fill of the chart element to have the default value.


```python
def set_default_fill(self):
    ...
```

### Examples

Shows how to reset the fill to the default value defined in the series.

```python
doc = Document(MY_DIR + "DataPoint format.docx")
shape = doc.get_child(aw.NodeType.SHAPE, 0, True).as_shape()

series = shape.chart.series[0]
data_point = series.data_points[1]

self.assertTrue(data_point.format.is_defined)

data_point.format.set_default_fill()

doc.save(ARTIFACTS_DIR + "Charts.ResetDataPointFill.docx")
```

### See Also

* module [aspose.words.drawing.charts](../../)
* class [ChartFormat](../)

