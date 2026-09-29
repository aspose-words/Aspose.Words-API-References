---
title: ChartAxis.axis_between_categories property
linktitle: axis_between_categories property
articleTitle: axis_between_categories property
second_title: Aspose.Words for Python
description: "ChartAxis.axis_between_categories property. Gets or sets a flag indicating whether the value axis crosses the category axis between categories."
type: docs
weight: 10
url: /it/python-net/aspose.words.drawing.charts/chartaxis/axis_between_categories/
---

## ChartAxis.axis_between_categories property

Gets or sets a flag indicating whether the value axis crosses the category axis between categories.


```python
@property
def axis_between_categories(self) -> bool:
    ...

@axis_between_categories.setter
def axis_between_categories(self, value: bool):
    ...

```

### Remarks

The property has effect only for value axes. It is not supported by MS Office 2016 new charts.


### Examples

Shows how to get a graph axis to cross at a custom location.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
shape = builder.insert_chart(chart_type=aw.drawing.charts.ChartType.COLUMN, width=450, height=250)
chart = shape.chart
self.assertEqual(3, chart.series.count)
self.assertEqual('Series 1', chart.series[0].name)
self.assertEqual('Series 2', chart.series[1].name)
self.assertEqual('Series 3', chart.series[2].name)
# Per i grafici a colonne, l'asse Y incrocia lo zero per impostazione predefinita,
# il che significa che le colonne per tutti i valori inferiori a zero puntano verso il basso per rappresentare i valori negativi.
# Possiamo impostare un valore diverso per l'incrocio dell'asse Y. In questo caso, lo imposteremo a 3.
axis = chart.axis_x
axis.crosses = aw.drawing.charts.AxisCrosses.CUSTOM
axis.crosses_at = 3
axis.axis_between_categories = True
doc.save(file_name=ARTIFACTS_DIR + 'Charts.AxisCross.docx')
```

### See Also

* module [aspose.words.drawing.charts](../../)
* class [ChartAxis](../)

