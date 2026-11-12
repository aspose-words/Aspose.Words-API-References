---
title: ChartSeries.legend_entry property
linktitle: legend_entry property
articleTitle: legend_entry property
second_title: Aspose.Words for Python
description: "ChartSeries.legend_entry property. Gets a legend entry for this chart series."
type: docs
weight: 90
url: /ru/python-net/aspose.words.drawing.charts/chartseries/legend_entry/
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
# Установить размер шрифта по умолчанию для всех элементов легенды.
chart_legend.font.size = 14
# Изменить шрифт для конкретного элемента легенды.
chart_legend.legend_entries[1].font.italic = True
chart_legend.legend_entries[1].font.size = 12
# Получить элемент легенды для серии диаграммы.
legend_entry = chart.series[0].legend_entry
doc.save(file_name=ARTIFACTS_DIR + 'Charts.LegendFont.docx')
```

### See Also

* module [aspose.words.drawing.charts](../../)
* class [ChartSeries](../)

