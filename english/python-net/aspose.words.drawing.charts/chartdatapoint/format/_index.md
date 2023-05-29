---
title: ChartDataPoint.format property
linktitle: format property
articleTitle: format property
second_title: Aspose.Words for Python
description: "ChartDataPoint.format property. Provides access to fill and line formatting of this data point."
type: docs
weight: 30
url: /python-net/aspose.words.drawing.charts/chartdatapoint/format/
---

## ChartDataPoint.format property

Provides access to fill and line formatting of this data point.


### Examples

Shows how to set individual formatting for categories of a column chart.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

shape = builder.insert_chart(aw.drawing.charts.ChartType.COLUMN, 432, 252)
chart = shape.chart

# Delete default generated series.
chart.series.clear()

# Adding new series.
series = chart.series.add("Series 1",
    ["Category 1", "Category 2", "Category 3", "Category 4"],
    [1, 2, 3, 4])

# Set column formatting.
data_points = series.data_points
data_points[0].format.fill.preset_textured(aw.drawing.PresetTexture.DENIM)
data_points[1].format.fill.fore_color = drawing.Color.red
data_points[2].format.fill.fore_color = drawing.Color.yellow
data_points[3].format.fill.fore_color = drawing.Color.blue

doc.save(ARTIFACTS_DIR + "Charts.data_points_formatting.docx")
```

### See Also

* module [aspose.words.drawing.charts](../../)
* class [ChartDataPoint](../)

