﻿---
title: ChartAxisTitle.font property
linktitle: font property
articleTitle: font property
second_title: Aspose.Words for Python
description: "ChartAxisTitle.font property. Provides access to the font formatting of the axis title."
type: docs
weight: 10
url: /python-net/aspose.words.drawing.charts/chartaxistitle/font/
---

## ChartAxisTitle.font property

Provides access to the font formatting of the axis title.


```python
@property
def font(self) -> aspose.words.Font:
    ...

```

### Examples

Shows how to set chart axis title.

```python
doc = Document()

builder = DocumentBuilder(doc)
shape = builder.insert_chart(ChartType.COLUMN, 432, 252)

chart = shape.chart

series_coll = chart.series
# Delete default generated series.
series_coll.clear()

series_coll.add("AW Series 1", ["AW Category 1", "AW Category 2"], [1, 2])

# Set axis title.
chart.axis_x.title.text = "Categories"
chart.axis_x.title.show = True
chart.axis_y.title.text = "Values"
chart.axis_y.title.show = True
chart.axis_y.title.overlay = True
chart.axis_y.title.font.size = 12
chart.axis_y.title.font.color = drawing.Color.blue

doc.save(ARTIFACTS_DIR + "Charts.ChartAxisTitle.docx")
```

### See Also

* module [aspose.words.drawing.charts](../../)
* class [ChartAxisTitle](../)

