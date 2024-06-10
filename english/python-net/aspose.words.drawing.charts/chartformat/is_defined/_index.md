---
title: ChartFormat.is_defined property
linktitle: is_defined property
articleTitle: is_defined property
second_title: Aspose.Words for Python
description: "ChartFormat.is_defined property. Gets a flag indicating whether any format is defined."
type: docs
weight: 20
url: /python-net/aspose.words.drawing.charts/chartformat/is_defined/
---

## ChartFormat.is_defined property

Gets a flag indicating whether any format is defined.


```python
@property
def is_defined(self) -> bool:
    ...

```

### Examples

Shows how to reset the fill to the default value defined in the series.

```python
doc = aw.Document(file_name=MY_DIR + 'DataPoint format.docx')
shape = doc.get_child(aw.NodeType.SHAPE, 0, True).as_shape()
series = shape.chart.series[0]
data_point = series.data_points[1]
self.assertTrue(data_point.format.is_defined)
data_point.format.set_default_fill()
doc.save(file_name=ARTIFACTS_DIR + 'Charts.ResetDataPointFill.docx')
```

### See Also

* module [aspose.words.drawing.charts](../../)
* class [ChartFormat](../)

