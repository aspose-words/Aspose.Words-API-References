---
title: ChartLegend.legend_entries property
linktitle: legend_entries property
articleTitle: legend_entries property
second_title: Aspose.Words for Python
description: "ChartLegend.legend_entries property. Returns a collection of legend entries for all series and trendlines of the parent chart."
type: docs
weight: 30
url: /python-net/aspose.words.drawing.charts/chartlegend/legend_entries/
---

## ChartLegend.legend_entries property

Returns a collection of legend entries for all series and trendlines of the parent chart.


```python
@property
def legend_entries(self) -> aspose.words.drawing.charts.ChartLegendEntryCollection:
    ...

```

### Examples

Shows how to work with a legend entry for chart series.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
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
* class [ChartLegend](../)

