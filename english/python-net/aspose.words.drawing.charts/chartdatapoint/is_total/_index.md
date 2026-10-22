---
title: ChartDataPoint.is_total property
linktitle: is_total property
articleTitle: is_total property
second_title: Aspose.Words for Python
description: "ChartDataPoint.is_total property. Gets a flag indicating whether the data point is a total"
type: docs
weight: 60
url: /python-net/aspose.words.drawing.charts/chartdatapoint/is_total/
---

## ChartDataPoint.is_total property

Gets a flag indicating whether the data point is a total. Applies only to Waterfall charts.


```python
@property
def is_total(self) -> bool:
    ...

```

### Remarks

In a waterfall chart, total columns represent intermediate or final totals.
If this property returns **true**, the data point is such a total column.



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
* class [ChartDataPoint](../)

