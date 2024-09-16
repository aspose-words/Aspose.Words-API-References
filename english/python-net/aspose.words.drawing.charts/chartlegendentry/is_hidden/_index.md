---
title: ChartLegendEntry.is_hidden property
linktitle: is_hidden property
articleTitle: is_hidden property
second_title: Aspose.Words for Python
description: "ChartLegendEntry.is_hidden property. Gets or sets a value indicating whether this entry is hidden in the chart legend"
type: docs
weight: 20
url: /python-net/aspose.words.drawing.charts/chartlegendentry/is_hidden/
---

## ChartLegendEntry.is_hidden property

Gets or sets a value indicating whether this entry is hidden in the chart legend.
The default value is **false**.



```python
@property
def is_hidden(self) -> bool:
    ...

@is_hidden.setter
def is_hidden(self, value: bool):
    ...

```

### Remarks

When a chart legend entry is hidden, it does not affect the corresponding chart series or trendline that
is still displayed on the chart.


### Examples

Shows how to work with a legend entry for chart series.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
shape = builder.insert_chart(chart_type=aw.drawing.charts.ChartType.COLUMN, width=432, height=252)
chart = shape.chart
series = chart.series
series.clear()
categories = ['AW Category 1', 'AW Category 2']
series1 = series.add(series_name='Series 1', categories=categories, values=[1, 2])
series.add(series_name='Series 2', categories=categories, values=[3, 4])
series.add(series_name='Series 3', categories=categories, values=[5, 6])
series.add(series_name='Series 4', categories=categories, values=[0, 0])
legend_entries = chart.legend.legend_entries
legend_entries[3].is_hidden = True
doc.save(file_name=ARTIFACTS_DIR + 'Charts.LegendEntries.docx')
```

### See Also

* module [aspose.words.drawing.charts](../../)
* class [ChartLegendEntry](../)

