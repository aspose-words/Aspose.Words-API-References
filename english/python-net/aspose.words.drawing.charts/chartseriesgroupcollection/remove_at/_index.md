---
title: ChartSeriesGroupCollection.remove_at method
linktitle: remove_at method
articleTitle: remove_at method
second_title: Aspose.Words for Python
description: "ChartSeriesGroupCollection.remove_at method. Removes a series group at the specified index"
type: docs
weight: 40
url: /python-net/aspose.words.drawing.charts/chartseriesgroupcollection/remove_at/
---

## remove_at(index) {#int}

Removes a series group at the specified index. All child series will be removed from the chart.


```python
def remove_at(self, index: int):
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

