---
title: ChartSeries.legend_entry property
linktitle: legend_entry property
articleTitle: legend_entry property
second_title: Aspose.Words for Python
description: "ChartSeries.legend_entry property. Gets a legend entry for this chart series."
type: docs
weight: 90
url: /it/python-net/aspose.words.drawing.charts/chartseries/legend_entry/
---

## ChartSeries.legend_entry property

Gets a legend entry for this chart series.


```python
@property
def legend_entry(self) -> aspose.words.drawing.charts.ChartLegendEntry:
    ...

```

### Examples

Shows how to work with a legend font.

```python
doc = aw.Document(file_name=MY_DIR + 'Reporting engine template - Chart series.docx')
chart = doc.get_child(aw.NodeType.SHAPE, 0, True).as_shape().chart
chart_legend = chart.legend
# Imposta la dimensione predefinita del carattere per tutte le voci della legenda.
chart_legend.font.size = 14
# Cambia il carattere per una voce specifica della legenda.
chart_legend.legend_entries[1].font.italic = True
chart_legend.legend_entries[1].font.size = 12
# Ottieni la voce della legenda per la serie del grafico.
legend_entry = chart.series[0].legend_entry
doc.save(file_name=ARTIFACTS_DIR + 'Charts.LegendFont.docx')
```

### See Also

* module [aspose.words.drawing.charts](../../)
* class [ChartSeries](../)

