---
title: ChartSeriesGroup.series_type property
linktitle: series_type property
articleTitle: series_type property
second_title: Aspose.Words for Python
description: "ChartSeriesGroup.series_type property. Gets the type of chart series included in this group."
type: docs
weight: 110
url: /sv/python-net/aspose.words.drawing.charts/chartseriesgroup/series_type/
---

## ChartSeriesGroup.series_type property

Gets the type of chart series included in this group.


```python
@property
def series_type(self) -> aspose.words.drawing.charts.ChartSeriesType:
    ...

```

### Examples

Shows how to work with the secondary axis of chart.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
shape = builder.insert_chart(chart_type=aw.drawing.charts.ChartType.LINE, width=450, height=250)
chart = shape.chart
series = chart.series
# Ta bort standardgenererad serie.
series.clear()
categories = ['Category 1', 'Category 2', 'Category 3']
series.add(series_name='Series 1 of primary series group', categories=categories, values=[2, 3, 4])
series.add(series_name='Series 2 of primary series group', categories=categories, values=[5, 2, 3])
# Skapa en extra seriegroupp, också av linjetyp.
new_series_group = chart.series_groups.add(aw.drawing.charts.ChartSeriesType.LINE)
# Ange användning av sekundära axlar för den nya seriegrouppen.
new_series_group.axis_group = aw.drawing.charts.AxisGroup.SECONDARY
# Dölj den sekundära X-axeln.
new_series_group.axis_x.hidden = True
# Definiera titel för den sekundära Y-axeln.
new_series_group.axis_y.title.show = True
new_series_group.axis_y.title.text = 'Secondary Y axis'
self.assertEqual(aw.drawing.charts.ChartSeriesType.LINE, new_series_group.series_type)
# Lägg till en serie i den nya seriegrouppen.
series3 = new_series_group.series.add(series_name='Series of secondary series group', categories=categories, values=[13, 11, 16])
series3.format.stroke.weight = 3.5
doc.save(file_name=ARTIFACTS_DIR + 'Charts.SecondaryAxis.docx')
```

### See Also

* module [aspose.words.drawing.charts](../../)
* class [ChartSeriesGroup](../)

