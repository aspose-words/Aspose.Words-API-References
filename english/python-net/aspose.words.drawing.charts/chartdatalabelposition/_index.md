---
title: ChartDataLabelPosition enumeration
linktitle: ChartDataLabelPosition enumeration
articleTitle: ChartDataLabelPosition enumeration
second_title: Aspose.Words for Python
description: "aspose.words.drawing.charts.ChartDataLabelPosition enumeration. Specifies the position for a chart data label."
type: docs
weight: 220
url: /python-net/aspose.words.drawing.charts/chartdatalabelposition/
---

## ChartDataLabelPosition enumeration

Specifies the position for a chart data label.

Not all series types allow you to specify label positions. And those that do, do not support all values.


### Members

| Name | Description |
| --- | --- |
| CENTER | Specifies that a data label should be displayed centered on a data marker. |
| LEFT | Specifies that a data label should be displayed to the left of a data marker. |
| RIGHT | Specifies that a data label should be displayed to the right of a data marker. |
| ABOVE | Specifies that a data label should be displayed above a data marker. |
| BELOW | Specifies that a data label should be displayed below a data marker. |
| INSIDE_BASE | Specifies that a data label should be displayed inside the base of a data marker. |
| INSIDE_END | Specifies that a data label should be displayed inside the end of a data marker. |
| OUTSIDE_END | Specifies that a data label should be displayed outside the end of a data marker. |
| BEST_FIT | Specifies that a data label should be displayed in the most appropriate position. |

### Examples

Shows how to set the position of the data label.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Insert column chart.
shape = builder.insert_chart(chart_type=aw.drawing.charts.ChartType.COLUMN, width=432, height=252)
chart = shape.chart
series_coll = chart.series
# Delete default generated series.
series_coll.clear()
# Add series.
series = series_coll.add(series_name='Series 1', categories=['Category 1', 'Category 2', 'Category 3'], values=[4, 5, 6])
# Show data labels and set font color.
series.has_data_labels = True
data_labels = series.data_labels
data_labels.show_value = True
data_labels.font.color = aspose.pydrawing.Color.white
# Set data label position.
data_labels.position = aw.drawing.charts.ChartDataLabelPosition.INSIDE_BASE
data_labels[0].position = aw.drawing.charts.ChartDataLabelPosition.OUTSIDE_END
data_labels[0].font.color = aspose.pydrawing.Color.dark_red
doc.save(file_name=ARTIFACTS_DIR + 'Charts.LabelPosition.docx')
```

### See Also

* module [aspose.words.drawing.charts](../)

