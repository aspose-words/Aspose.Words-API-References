---
title: ChartSeries.is_total method
linktitle: is_total method
articleTitle: is_total method
second_title: Aspose.Words for Python
description: "ChartSeries.is_total method. Determines whether the data point at the specified index is a total"
type: docs
weight: 210
url: /python-net/aspose.words.drawing.charts/chartseries/is_total/
---

## is_total(index) {#int}

Determines whether the data point at the specified index is a total.
Applies only to Waterfall charts.


```python
def is_total(self, index: int):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| index | int | The zero-based index of the data point. |

### Returns

**true** if the data point is a total; otherwise, **false**.


### Examples

Shows how to determine whether a data point is a total in a waterfall chart.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Insert a Waterfall chart.
shape = builder.insert_chart(chart_type=aw.drawing.charts.ChartType.WATERFALL, width=450, height=450)
chart = shape.chart
chart.title.text = "New Zealand GDP"
# Delete default generated series.
chart.series.clear()
# Add a series where the start value, the subtotal and the final value are totals.
series = chart.series.add(series_name="New Zealand GDP", categories=["2018", "2019 growth", "2020 growth", "2020", "2021 growth", "2022 growth", "2022"], values=[100, 0.57, -0.25, 100.32, 20.22, -2.92, 117.62], is_subtotal=[True, False, False, True, False, False, True])
# Print the type of each data point.
i = 0
while i < series.y_values.count:
    if series.is_total(i):
        print(f"Data point {i} is Subtotal")
    elif series.y_values[i].double_value > 0:
        print(f"Data point {i} is Increase")
    else:
        print(f"Data point {i} is Decrease")
    i += 1
# The same flag is available on the data point itself.
print(f"Data point 3 is total: {series.data_points[3].is_total}")
doc.save(file_name=ARTIFACTS_DIR + "Charts.ChartSeriesAndDataPointIsTotal.docx")
```

### See Also

* module [aspose.words.drawing.charts](../../)
* class [ChartSeries](../)

