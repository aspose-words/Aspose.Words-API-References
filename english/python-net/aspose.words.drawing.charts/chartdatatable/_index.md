---
title: ChartDataTable class
linktitle: ChartDataTable class
articleTitle: ChartDataTable class
second_title: Aspose.Words for Python
description: "aspose.words.drawing.charts.ChartDataTable class. Allows to specify properties of a chart data table."
type: docs
weight: 230
url: /python-net/aspose.words.drawing.charts/chartdatatable/
---

## ChartDataTable class

Allows to specify properties of a chart data table.


### Properties

| Name | Description |
| --- | --- |
| [font](./font/) | Provides access to font formatting of the data table. |
| [format](./format/) | Provides access to fill of text background and border formatting of the data table. |
| [has_horizontal_border](./has_horizontal_border/) | Gets or sets a flag indicating whether a horizontal border of the data table is displayed. The default value is ``True``. |
| [has_legend_keys](./has_legend_keys/) | Gets or sets a flag indicating whether legend keys are displayed in the data table. The default value is ``True``. |
| [has_outline_border](./has_outline_border/) | Gets or sets a flag indicating whether an outline border, that is, a border around series and category names, is displayed. The default value is ``True``. |
| [has_vertical_border](./has_vertical_border/) | Gets or sets a flag indicating whether a vertical border of the data table is displayed. The default value is ``True``. |
| [show](./show/) | Gets or sets a flag indicating whether the data table will be shown for the chart. Default value is ``False``. |

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
data_table.font.italic = True
data_table.format.stroke.weight = 1
data_table.format.stroke.dash_style = aw.drawing.DashStyle.SHORT_DOT
data_table.format.stroke.color = aspose.pydrawing.Color.dark_blue
doc.save(file_name=ARTIFACTS_DIR + 'Charts.DataTable.docx')
```

### See Also

* module [aspose.words.drawing.charts](../)

