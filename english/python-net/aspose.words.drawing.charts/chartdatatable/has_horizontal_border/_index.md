---
title: ChartDataTable.has_horizontal_border property
linktitle: has_horizontal_border property
articleTitle: has_horizontal_border property
second_title: Aspose.Words for Python
description: "ChartDataTable.has_horizontal_border property. Gets or sets a flag indicating whether a horizontal border of the data table is displayed"
type: docs
weight: 30
url: /python-net/aspose.words.drawing.charts/chartdatatable/has_horizontal_border/
---

## ChartDataTable.has_horizontal_border property

Gets or sets a flag indicating whether a horizontal border of the data table is displayed.
The default value is ``True``.



```python
@property
def has_horizontal_border(self) -> bool:
    ...

@has_horizontal_border.setter
def has_horizontal_border(self, value: bool):
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
series.add(series_name='Series1', x_values=x_values, y_values=[5, 11, 2, 7])
series.add(series_name='Series2', x_values=x_values, y_values=[6, 5.5, 7, 7.8])
series.add(series_name='Series3', x_values=x_values, y_values=[10, 8, 7, 9])
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

