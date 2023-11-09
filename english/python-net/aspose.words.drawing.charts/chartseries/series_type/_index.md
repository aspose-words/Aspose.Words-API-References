---
title: ChartSeries.series_type property
linktitle: series_type property
articleTitle: series_type property
second_title: Aspose.Words for Python
description: "ChartSeries.series_type property. Gets the type of this chart series."
type: docs
weight: 120
url: /python-net/aspose.words.drawing.charts/chartseries/series_type/
---

## ChartSeries.series_type property

Gets the type of this chart series.


```python
@property
def series_type(self) -> aspose.words.drawing.charts.ChartSeriesType:
    ...

```

### Examples

Shows how to remove specific chart series

```python
doc = Document(MY_DIR + "Reporting engine template - Chart series.docx")
chart = doc.get_child(NodeType.SHAPE, 0, True).as_shape().chart

# Remove all series of the Column type.
for i in range(0, chart.series.count, -1):
    if chart.series[i].series_type == ChartSeriesType.COLUMN:
        chart.series.remove(i)

chart.series.add("Aspose Series", ["Category 1", "Category 2", "Category 3", "Category 4"],
                 [5.6, 7.1, 2.9, 8.9])

doc.save(ARTIFACTS_DIR + "Charts.RemoveSpecificChartSeries.docx")
```

### See Also

* module [aspose.words.drawing.charts](../../)
* class [ChartSeries](../)

