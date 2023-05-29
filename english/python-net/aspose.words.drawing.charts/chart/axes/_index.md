---
title: Chart.axes property
linktitle: axes property
articleTitle: axes property
second_title: Aspose.Words for Python
description: "Chart.axes property. Gets a collection of all axes of this chart."
type: docs
weight: 10
url: /python-net/aspose.words.drawing.charts/chart/axes/
---

## Chart.axes property

Gets a collection of all axes of this chart.


### Examples

Shows how to work with axes collection.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

shape = builder.insert_chart(awdc.ChartType.COLUMN, 500, 300)
chart = shape.chart

# Hide the major grid lines on the primary and secondary Y axes.
for axis in chart.axes:
    if axis.type == awdc.ChartAxisType.VALUE:
        axis.has_major_gridlines = False

doc.save(ARTIFACTS_DIR + "Charts.AxisCollection.docx")
```

### See Also

* module [aspose.words.drawing.charts](../../)
* class [Chart](../)

