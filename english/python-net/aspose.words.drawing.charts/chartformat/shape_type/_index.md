---
title: ChartFormat.shape_type property
linktitle: shape_type property
articleTitle: shape_type property
second_title: Aspose.Words for Python
description: "ChartFormat.shape_type property. Gets or sets the shape type of the parent chart element."
type: docs
weight: 30
url: /python-net/aspose.words.drawing.charts/chartformat/shape_type/
---

## ChartFormat.shape_type property

Gets or sets the shape type of the parent chart element.

Currently, the property can only be used for data labels.


### Examples

Shows how to set fill, stroke and callout formatting for chart data labels.

```python
doc = Document()
builder = DocumentBuilder(doc)

shape = builder.insert_chart(ChartType.COLUMN, 432, 252)
chart = shape.chart

# Delete default generated series.
chart.series.clear()

# Add new series.
series = chart.series.add("AW Series 1", ["AW Category 1", "AW Category 2", "AW Category 3", "AW Category 4"],
                          [100, 200, 300, 400])

# Show data labels.
series.has_data_labels = True
series.data_labels.show_value = True

# Format data labels as callouts.
format = series.data_labels.format
format.shape_type = ChartShapeType.WEDGE_RECT_CALLOUT
format.stroke.color = Color.dark_green
format.fill.solid(Color.green)
series.data_labels.font.color = Color.yellow

# Change fill and stroke of an individual data label.
labelFormat = series.data_labels[0].format
labelFormat.stroke.color = Color.dark_blue
labelFormat.fill.solid(Color.blue)

doc.save(ARTIFACTS_DIR + "Charts.FormatDataLabels.docx")
```

### See Also

* module [aspose.words.drawing.charts](../../)
* class [ChartFormat](../)

