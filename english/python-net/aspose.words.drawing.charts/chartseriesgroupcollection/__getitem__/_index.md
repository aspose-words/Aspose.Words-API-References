---
title: ChartSeriesGroupCollection indexer
linktitle: ChartSeriesGroupCollection indexer
articleTitle: ChartSeriesGroupCollection indexer
second_title: Aspose.Words for Python
description: "ChartSeriesGroupCollection indexer. Returns a [ChartSeriesGroup](../../chartseriesgroup/) at the specified index."
type: docs
weight: 10
url: /python-net/aspose.words.drawing.charts/chartseriesgroupcollection/__getitem__/
---

## \_\_getitem\_\_(index) {#int}

Returns a [ChartSeriesGroup](../../chartseriesgroup/) at the specified index.



```python
def __getitem__(self, index: int):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| index | int |  |

### Examples

Show how to remove secondary axis.

```python
doc = aw.Document(file_name=MY_DIR + 'Combo chart.docx')
shape = doc.get_child(aw.NodeType.SHAPE, 0, True).as_shape()
chart = shape.chart
series_groups = chart.series_groups
# Find secondary axis and remove from the collection.
i = 0
while i < series_groups.count:
    if series_groups[i].axis_group == aw.drawing.charts.AxisGroup.SECONDARY:
        series_groups.remove_at(i)
    i += 1
```

### See Also

* module [aspose.words.drawing.charts](../../)
* class [ChartSeriesGroupCollection](../)

