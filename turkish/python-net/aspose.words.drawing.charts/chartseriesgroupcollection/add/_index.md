---
title: ChartSeriesGroupCollection.add method
linktitle: add method
articleTitle: add method
second_title: Aspose.Words for Python
description: "ChartSeriesGroupCollection.add method. Adds a new series group of the specified series type to this collection."
type: docs
weight: 30
url: /tr/python-net/aspose.words.drawing.charts/chartseriesgroupcollection/add/
---

## add(series_type) {#chartseriestype}

Adds a new series group of the specified series type to this collection.


```python
def add(self, series_type: aspose.words.drawing.charts.ChartSeriesType):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| series_type | [ChartSeriesType](../../chartseriestype/) |  |

### Remarks

Combo charts can contain series groups only of the following types: area, bar, column, line, pie, scatter,
radar and stock types (except the corresponding 3D series types).


### Examples

Shows how to work with the secondary axis of chart.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
shape = builder.insert_chart(chart_type=aw.drawing.charts.ChartType.LINE, width=450, height=250)
chart = shape.chart
series = chart.series
# Varsayılan oluşturulan seriyi sil.
series.clear()
categories = ['Category 1', 'Category 2', 'Category 3']
series.add(series_name='Series 1 of primary series group', categories=categories, values=[2, 3, 4])
series.add(series_name='Series 2 of primary series group', categories=categories, values=[5, 2, 3])
# Satır tipi olan ek bir seri grubu oluşturun.
new_series_group = chart.series_groups.add(aw.drawing.charts.ChartSeriesType.LINE)
# Yeni seri grubu için ikincil eksenlerin kullanımını belirtin.
new_series_group.axis_group = aw.drawing.charts.AxisGroup.SECONDARY
# İkincil X eksenini gizleyin.
new_series_group.axis_x.hidden = True
# İkincil Y ekseninin başlığını tanımlayın.
new_series_group.axis_y.title.show = True
new_series_group.axis_y.title.text = 'Secondary Y axis'
self.assertEqual(aw.drawing.charts.ChartSeriesType.LINE, new_series_group.series_type)
# Yeni seri grubuna bir seri ekleyin.
series3 = new_series_group.series.add(series_name='Series of secondary series group', categories=categories, values=[13, 11, 16])
series3.format.stroke.weight = 3.5
doc.save(file_name=ARTIFACTS_DIR + 'Charts.SecondaryAxis.docx')
```

### See Also

* module [aspose.words.drawing.charts](../../)
* class [ChartSeriesGroupCollection](../)

