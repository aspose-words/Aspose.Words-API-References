---
title: ChartSeriesGroup.doughnut_hole_size property
linktitle: doughnut_hole_size property
articleTitle: doughnut_hole_size property
second_title: Aspose.Words for Python
description: "ChartSeriesGroup.doughnut_hole_size property. Gets or sets the hole size of the parent doughnut chart as a percentage."
type: docs
weight: 50
url: /python-net/aspose.words.drawing.charts/chartseriesgroup/doughnut_hole_size/
---

## ChartSeriesGroup.doughnut_hole_size property

Gets or sets the hole size of the parent doughnut chart as a percentage.


```python
@property
def doughnut_hole_size(self) -> int:
    ...

@doughnut_hole_size.setter
def doughnut_hole_size(self, value: int):
    ...

```

### Remarks

Applies only to series groups of the [ChartSeriesType.DOUGHNUT](../../chartseriestype/#DOUGHNUT) type.

The range of acceptable values is from 0 to 90 inclusive. The default value is 75.




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

