---
title: ChartDataTable.format property
linktitle: format property
articleTitle: format property
second_title: Aspose.Words for Python
description: "ChartDataTable.format property. Provides access to fill of text background and border formatting of the data table."
type: docs
weight: 20
url: /python-net/aspose.words.drawing.charts/chartdatatable/format/
---

## ChartDataTable.format property

Provides access to fill of text background and border formatting of the data table.


```python
@property
def format(self) -> aspose.words.drawing.charts.ChartFormat:
    ...

```

### Examples

Shows how to show data table with chart series data.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
shape = builder.insert_chart(chart_type=aw.drawing.charts.ChartType.COLUMN, width=432, height=252)
chart = shape.chart
series = chart.series
series.clear()
x_values = [2020, 2021, 2022, 2023]
series.add_double(series_name='Series1', x_values=x_values, y_values=[5, 11, 2, 7])
series.add_double(series_name='Series2', x_values=x_values, y_values=[6, 5.5, 7, 7.8])
series.add_double(series_name='Series3', x_values=x_values, y_values=[10, 8, 7, 9])
data_table = chart.data_table
data_table.show = True
data_table.has_legend_keys = False
data_table.has_horizontal_border = False
data_table.has_vertical_border = False
data_table.has_outline_border = False
data_table.font.italic = True
data_table.format.stroke.weight = 1
data_table.format.stroke.dash_style = aw.drawing.DashStyle.SHORT_DOT
data_table.format.stroke.color = aspose.pydrawing.Color.dark_blue
doc.save(file_name=ARTIFACTS_DIR + 'Charts.DataTable.docx')
```

### See Also

* module [aspose.words.drawing.charts](../../)
* class [ChartDataTable](../)

