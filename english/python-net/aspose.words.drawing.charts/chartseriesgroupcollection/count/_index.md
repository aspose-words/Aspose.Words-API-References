---
title: ChartSeriesGroupCollection.count property
linktitle: count property
articleTitle: count property
second_title: Aspose.Words for Python
description: "ChartSeriesGroupCollection.count property. Returns the number of series groups in this collection."
type: docs
weight: 20
url: /python-net/aspose.words.drawing.charts/chartseriesgroupcollection/count/
---

## ChartSeriesGroupCollection.count property

Returns the number of series groups in this collection.


```python
@property
def count(self) -> int:
    ...

```

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

