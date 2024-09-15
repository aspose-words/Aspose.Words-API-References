---
title: ChartSeriesGroup.gap_width property
linktitle: gap_width property
articleTitle: gap_width property
second_title: Aspose.Words for Python
description: "ChartSeriesGroup.gap_width property. Gets or sets the percentage of gap width between chart elements."
type: docs
weight: 50
url: /python-net/aspose.words.drawing.charts/chartseriesgroup/gap_width/
---

## ChartSeriesGroup.gap_width property

Gets or sets the percentage of gap width between chart elements.


```python
@property
def gap_width(self) -> int:
    ...

@gap_width.setter
def gap_width(self, value: int):
    ...

```

### Remarks

Applies only to series groups of the bar, column, pie-of-bar, pie-of-pie, histogram, box&whisker,
waterfall and funnel types.

The range of acceptable values is from 0 to 500 inclusive. For bar/column-based series groups, the
property represents the space between bar clusters as a percentage of their width. For pie-of-pie and
bar-of-pie charts, this is the space between the primary and secondary sections of the chart.




### Examples

Show how to configure gap width and overlap.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
shape = builder.insert_chart(chart_type=aw.drawing.charts.ChartType.COLUMN, width=450, height=250)
series_group = shape.chart.series_groups[0]
# Set column gap width and overlap.
series_group.gap_width = 450
series_group.overlap = -75
doc.save(file_name=ARTIFACTS_DIR + 'Charts.ConfigureGapOverlap.docx')
```

### See Also

* module [aspose.words.drawing.charts](../../)
* class [ChartSeriesGroup](../)

