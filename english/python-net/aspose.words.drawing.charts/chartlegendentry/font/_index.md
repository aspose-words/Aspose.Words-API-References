---
title: ChartLegendEntry.font property
linktitle: font property
articleTitle: font property
second_title: Aspose.Words for Python
description: "ChartLegendEntry.font property. Provides access to the font formatting of this legend entry."
type: docs
weight: 10
url: /python-net/aspose.words.drawing.charts/chartlegendentry/font/
---

## ChartLegendEntry.font property

Provides access to the font formatting of this legend entry.


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

for legend_entry in legend_entries:
    legend_entry.font.size = 12

series1.legend_entry.font.italic = True

doc.save(ARTIFACTS_DIR + "Charts.LegendEntries.docx")
```

### See Also

* module [aspose.words.drawing.charts](../../)
* class [ChartLegendEntry](../)

