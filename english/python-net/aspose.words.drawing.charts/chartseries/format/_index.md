---
title: format property
second_title: Aspose.Words for Python via .NET API Reference
description: "Provides access to fill and line formatting of the series."
type: docs
weight: 50
url: /python-net/aspose.words.drawing.charts/chartseries/format/
---

## ChartSeries.format property

Provides access to fill and line formatting of the series.


### Examples

Sows how to set series color.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

shape = builder.insert_chart(aw.drawing.charts.ChartType.COLUMN, 432, 252)

chart = shape.chart
series_coll = chart.series

# Delete default generated series.
series_coll.clear()

# Create category names array.
categories = ["Category 1", "Category 2"]

# Adding new series. Value and category arrays must be the same size.
series1 = series_coll.add("Series 1", categories, [1, 2])
series2 = series_coll.add("Series 2", categories, [3, 4])
series3 = series_coll.add("Series 3", categories, [5, 6])

# Set series color.
series1.format.fill.fore_color = drawing.Color.red
series2.format.fill.fore_color = drawing.Color.yellow
series3.format.fill.fore_color = drawing.Color.blue

doc.save(ARTIFACTS_DIR + "Charts.series_color.docx")
```

### See Also

* module [aspose.words.drawing.charts](../../)
* class [ChartSeries](../)

