---
title: ChartLegendEntryCollection class
linktitle: ChartLegendEntryCollection class
articleTitle: ChartLegendEntryCollection class
second_title: Aspose.Words for Python
description: "aspose.words.drawing.charts.ChartLegendEntryCollection class. Represents a collection of chart legend entries"
type: docs
weight: 260
url: /python-net/aspose.words.drawing.charts/chartlegendentrycollection/
---

## ChartLegendEntryCollection class

Represents a collection of chart legend entries.
To learn more, visit the [Working with Charts](https://docs.aspose.com/words/python-net/working-with-charts/) documentation article.




### Indexers

| Name | Description |
| --- | --- |
| [``__getitem__(index)``](./__getitem__/#int) | Returns [ChartLegendEntry](../chartlegendentry/) for the specified index. |

### Properties

| Name | Description |
| --- | --- |
| [count](./count/) | Returns the number of [ChartLegendEntry](../chartlegendentry/) in this collection. |

### Examples

Shows how to work with a legend entry for chart series.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

shape = builder.insert_chart(awdc.ChartType.COLUMN, 432, 252)

chart = shape.chart
series = chart.series
series.clear()

categories = ["AW Category 1", "AW Category 2"]
series1 = series.add("Series 1", categories, [1, 2])
series.add("Series 2", categories, [3, 4])
series.add("Series 3", categories, [5, 6])
series.add("Series 4", categories, [0, 0])

legend_entries = chart.legend.legend_entries
legend_entries[3].is_hidden = True

doc.save(ARTIFACTS_DIR + "Charts.LegendEntries.docx")
```

### See Also

* module [aspose.words.drawing.charts](../)

