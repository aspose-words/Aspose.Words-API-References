---
title: ChartAxis.crosses_at property
linktitle: crosses_at property
articleTitle: crosses_at property
second_title: Aspose.Words for Python
description: "ChartAxis.crosses_at property. Specifies where on the perpendicular axis the axis crosses."
type: docs
weight: 50
url: /python-net/aspose.words.drawing.charts/chartaxis/crosses_at/
---

## ChartAxis.crosses_at property

Specifies where on the perpendicular axis the axis crosses.


```python
@property
def crosses_at(self) -> float:
    ...

@crosses_at.setter
def crosses_at(self, value: float):
    ...

```

### Remarks

The property has effect only if [ChartAxis.crosses](../crosses/) are set to [AxisCrosses.CUSTOM](../../axiscrosses/#CUSTOM).
It is not supported by MS Office 2016 new charts.

The units are determined by the type of axis. When the axis is a value axis, the value of the property
is a decimal number on the value axis. When the axis is a time category axis, the value is defined as
an integer number of days relative to the base date (30/12/1899). For a text category axis, the value is
an integer category number, starting with 1 as the first category.




### Examples

Shows how to get a graph axis to cross at a custom location.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

shape = builder.insert_chart(aw.drawing.charts.ChartType.COLUMN, 450, 250)
chart = shape.chart

self.assertEqual(3, chart.series.count)
self.assertEqual("Series 1", chart.series[0].name)
self.assertEqual("Series 2", chart.series[1].name)
self.assertEqual("Series 3", chart.series[2].name)

# For column charts, the Y-axis crosses at zero by default,
# which means that columns for all values below zero point down to represent negative values.
# We can set a different value for the Y-axis crossing. In this case, we will set it to 3.
axis = chart.axis_x
axis.crosses = aw.drawing.charts.AxisCrosses.CUSTOM
axis.crosses_at = 3
axis.axis_between_categories = True

doc.save(ARTIFACTS_DIR + "Charts.axis_cross.docx")
```

### See Also

* module [aspose.words.drawing.charts](../../)
* class [ChartAxis](../)

