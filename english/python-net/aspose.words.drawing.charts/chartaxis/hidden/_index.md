---
title: ChartAxis.hidden property
linktitle: hidden property
articleTitle: hidden property
second_title: Aspose.Words for Python
description: "ChartAxis.hidden property. Gets or sets a flag indicating whether this axis is hidden or not."
type: docs
weight: 100
url: /python-net/aspose.words.drawing.charts/chartaxis/hidden/
---

## ChartAxis.hidden property

Gets or sets a flag indicating whether this axis is hidden or not.

Default value is ``False``.



### Examples

Shows how to hide chart axes.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

shape = builder.insert_chart(aw.drawing.charts.ChartType.LINE, 500, 300)
chart = shape.chart

# Clear the chart's demo data series to start with a clean chart.
chart.series.clear()

# Add a custom series with categories for the X-axis, and respective decimal values for the Y-axis.
chart.series.add("AW Series 1",
    ["Item 1", "Item 2", "Item 3", "Item 4", "Item 5"],
    [1.2, 0.3, 2.1, 2.9, 4.2])

# Hide the chart axes to simplify the appearance of the chart.
chart.axis_x.hidden = True
chart.axis_y.hidden = True

doc.save(ARTIFACTS_DIR + "Charts.hide_chart_axis.docx")
```

### See Also

* module [aspose.words.drawing.charts](../../)
* class [ChartAxis](../)

