---
title: Chart.series_groups property
linktitle: series_groups property
articleTitle: series_groups property
second_title: Aspose.Words for Python
description: "Chart.series_groups property. Provides access to a series group collection of this chart."
type: docs
weight: 90
url: /python-net/aspose.words.drawing.charts/chart/series_groups/
---

## Chart.series_groups property

Provides access to a series group collection of this chart.


```python
@property
def series_groups(self) -> aspose.words.drawing.charts.ChartSeriesGroupCollection:
    ...

```

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
* class [Chart](../)

