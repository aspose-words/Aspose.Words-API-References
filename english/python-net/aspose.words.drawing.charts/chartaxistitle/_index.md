﻿---
title: ChartAxisTitle class
linktitle: ChartAxisTitle class
articleTitle: ChartAxisTitle class
second_title: Aspose.Words for Python
description: "aspose.words.drawing.charts.ChartAxisTitle class. Provides access to the axis title properties"
type: docs
weight: 150
url: /python-net/aspose.words.drawing.charts/chartaxistitle/
---

## ChartAxisTitle class

Provides access to the axis title properties.
To learn more, visit the [Working with
            Charts](https://docs.aspose.com/words/python-net/working-with-charts/) documentation article.




### Properties

| Name | Description |
| --- | --- |
| [overlay](./overlay/) | Determines whether other chart elements shall be allowed to overlap the title. The default value is ``False``. |
| [show](./show/) | Determines whether the title shall be shown for the axis. The default value is ``False``. |
| [text](./text/) | Gets or sets the text of the axis title. If ``None`` or empty value is specified, auto generated title will be shown. |

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

doc.save(ARTIFACTS_DIR + "Charts.ChartAxisTitle.docx")
```

### See Also

* module [aspose.words.drawing.charts](../)

