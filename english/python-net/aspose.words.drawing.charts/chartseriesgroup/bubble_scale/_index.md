---
title: ChartSeriesGroup.bubble_scale property
linktitle: bubble_scale property
articleTitle: bubble_scale property
second_title: Aspose.Words for Python
description: "ChartSeriesGroup.bubble_scale property. Gets or sets the size of the bubbles as a percentage of their default size."
type: docs
weight: 40
url: /python-net/aspose.words.drawing.charts/chartseriesgroup/bubble_scale/
---

## ChartSeriesGroup.bubble_scale property

Gets or sets the size of the bubbles as a percentage of their default size.


```python
@property
def bubble_scale(self) -> int:
    ...

@bubble_scale.setter
def bubble_scale(self, value: int):
    ...

```

### Remarks

Applies only to series groups of the [ChartSeriesType.BUBBLE](../../chartseriestype/#BUBBLE) and
[ChartSeriesType.BUBBLE_3D](../../chartseriestype/#BUBBLE_3D) types.

The range of acceptable values is from 0 to 300 inclusive.




### Examples

Show how to set size of the bubbles.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
# Insert a bubble 3D chart.
shape = builder.insert_chart(chart_type=aw.drawing.charts.ChartType.BUBBLE_3D, width=450, height=250)
series_group = shape.chart.series_groups[0]
# Set bubble scale to 200%.
series_group.bubble_scale = 200
doc.save(file_name=ARTIFACTS_DIR + 'Charts.BubbleScale.docx')
```

### See Also

* module [aspose.words.drawing.charts](../../)
* class [ChartSeriesGroup](../)

