---
title: ChartSeriesGroup.overlap property
linktitle: overlap property
articleTitle: overlap property
second_title: Aspose.Words for Python
description: "ChartSeriesGroup.overlap property. Gets or sets the percentage of how much the series bars or columns overlap."
type: docs
weight: 60
url: /python-net/aspose.words.drawing.charts/chartseriesgroup/overlap/
---

## ChartSeriesGroup.overlap property

Gets or sets the percentage of how much the series bars or columns overlap.


```python
@property
def overlap(self) -> int:
    ...

@overlap.setter
def overlap(self, value: int):
    ...

```

### Remarks

Applies to series groups of all bar and column types.

The range of acceptable values is from -100 to 100 inclusive. A value of 0 indicates that there is no
space between bars/columns. If the value is -100, the distance between bars/columns is equal to their width.
A value of 100 means that the bars/columns overlap completely.




### Examples

Show how to configure gap width and overlap.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
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

