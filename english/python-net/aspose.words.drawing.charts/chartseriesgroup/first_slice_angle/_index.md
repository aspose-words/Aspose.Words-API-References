---
title: ChartSeriesGroup.first_slice_angle property
linktitle: first_slice_angle property
articleTitle: first_slice_angle property
second_title: Aspose.Words for Python
description: "ChartSeriesGroup.first_slice_angle property. Gets or sets the angle, in degrees, of the first slice of the parent pie chart."
type: docs
weight: 60
url: /python-net/aspose.words.drawing.charts/chartseriesgroup/first_slice_angle/
---

## ChartSeriesGroup.first_slice_angle property

Gets or sets the angle, in degrees, of the first slice of the parent pie chart.


```python
@property
def first_slice_angle(self) -> int:
    ...

@first_slice_angle.setter
def first_slice_angle(self, value: int):
    ...

```

### Remarks

Applies to series groups of the [ChartSeriesType.PIE](../../chartseriestype/#PIE), [ChartSeriesType.PIE_3D](../../chartseriestype/#PIE_3D)
and [ChartSeriesType.DOUGHNUT](../../chartseriestype/#DOUGHNUT) types.

The range of acceptable values is from 0 to 360 inclusive. The default value is 0.




### Examples

Shows how to create and format Doughnut chart.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
shape = builder.insert_chart(chart_type=aw.drawing.charts.ChartType.DOUGHNUT, width=400, height=400)
chart = shape.chart
# Delete the default generated series.
chart.series.clear()
categories = ['Category 1', 'Category 2', 'Category 3']
chart.series.add(series_name='Series 1', categories=categories, values=[4, 2, 5])
# Format the Doughnut chart.
series_group = chart.series_groups[0]
series_group.doughnut_hole_size = 10
series_group.first_slice_angle = 270
doc.save(file_name=ARTIFACTS_DIR + 'Charts.DoughnutChart.docx')
```

### See Also

* module [aspose.words.drawing.charts](../../)
* class [ChartSeriesGroup](../)

